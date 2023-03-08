:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

.. TODO: Delete the note below before merging new content to the main branch.

.. note::

   **This technote is a work-in-progress.**

Abstract
========

This document describes the different states of the Laser, both functionally and for individual CSCs. It describes what those states mean for the subsystems within the laser, and how the laser will be operated generally.

Laser Description
=================

The laser system will be mounted on platforms near the calibration screen, provided by EIE. The actual laser will sit inside an enclosure which will provide the necessary thermal environment it requires to run at room temperature. An electronics enclosure will sit on a pillar near the laser enclosure and will provide power and controls to the laser, in addition to the thermal control hardware.

1. Laser Enclosure

2. Electronics Enclosure

Functional State Diagram
========================

.. image:: /_static/state_diagram_1.png
   :target: ../_images/state_diagram_1.png
   :alt: Functional State Diagram


OFF 
   All Power Off (including to laser)

MAINTENANCE
   Power to thermal and monitoring system off, power to laser and PDU remain ON

QUIESCENT
   Temperature of laser enclosure same as dome temperature. Power to all systems ON

WARMUP
   Heaters turned on (SP1 enabled on thermal controller)

READY
   Temperature of laser enclosure in safe operating range (18-25C)

ON
   Key is turned ON manually. Laser can be commanded

EMITTING
   If safety interlocks OK, laser is emitting light

COOLDOWN
   Cooling fan turned on (SP2 enable on thermal controller)

Laser Operation
===============



.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
.. 
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
