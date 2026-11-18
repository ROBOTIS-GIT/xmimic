# Cyclo integration

The upstream base revision is recorded in `UPSTREAM`. This branch retains the
original X-Mimic training and evaluation code, MIT license, and third-party
notices, with the following integration changes.

- Accept an optional compiled scene directory and explicit contact-body mapping.
- Accept an ordered manifest of exact 50 Hz native reference states and verify
  the prepared files against their hashes.
- Record the robot's joint order, nominal pose, and action scale in checkpoints.
- Reject mixed checkpoint configurations and mismatched robots during evaluation.

The Cyclo task, robot scene and motion preparation, and Sim2Real exporter live
in `cyclo_mjlab`. The existing X-Mimic G1 entry points remain available.
