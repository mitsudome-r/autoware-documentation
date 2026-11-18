# Reference software stacks

A reference software stack is a software configuration that Autoware publishes and maintains as a recommended baseline. Its name resolves to the modules, the model versions, the parameters, the interfaces, and the platform requirements. For the definition, see [Reference design concepts](concepts.md#reference-software-stack).

## Stacks

| Stack               | Contents                                                                              | Used by                                                                                              |
| ------------------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| Rule-based Planning | Localization and perception, rule-based planning, control, and supporting modules.    | [Low-speed shuttle](families/low-speed-shuttle.md), [Indoor logistics](families/indoor-logistics.md) |
| Diffusion Planning  | A specified diffusion planner, the required inputs, trajectory checks, and control.   | [Low-speed shuttle](families/low-speed-shuttle.md)                                                   |
| Meteor-based        | A specified METEOR model, the runtime, the adapters, and supporting Autoware modules. | [Low-speed shuttle](families/low-speed-shuttle.md)                                                   |
| Vision Pilot        | AutoSteer, AutoSpeed, AutoDrive, and explicitly selected supporting modules.          | [Highway assistance](families/highway-assistance.md)                                                 |
| Fusion Pilot        | AutoE2E, input processing, the runtime, output adapters, and supporting modules.      | [Urban robotaxi](families/urban-robotaxi.md)                                                         |

The full manifest of each stack and the deployment profiles that it supports are not specified yet.

### Rule-based Planning

The modular stack of Autoware Core and Autoware Universe, with the rule-based planners. See [Autoware architecture 2.0](../design/autoware-architecture-v2/index.md).

### Diffusion Planning

The modular stack with the [Diffusion Planner](https://github.com/autowarefoundation/autoware_universe/tree/0.53.1/planning/autoware_diffusion_planner) as the trajectory generator. Autoware starts it with `planning_setting:=diffusion_planner`. See [Autoware architecture 2.0](../design/autoware-architecture-v2/index.md).

### Meteor-based

A configuration around [METEOR](https://github.com/tier4/METEOR), a reference E2E model for surround-view driving. See [Data, MLOps, and training](../design/autoware-architecture-v2/roadmap/data-mlops-and-training.md#meteor).

### Vision Pilot

[Vision Pilot](https://github.com/autowarefoundation/vision_pilot) is an open-source, camera-based end-to-end Level 2 ADAS system.

### Fusion Pilot

A configuration around [AutoE2E](https://github.com/autowarefoundation/auto_e2e), an open-source, camera-first E2E driving model. Fusion Pilot adds the input processing and the output adapters for camera and LiDAR inputs.

## Manifest contents

The manifest of a stack lists:

- the modules and the packages, with their versions
- the models, with their versions and the location of their weights
- the parameters
- the input and the output interfaces
- the platform requirements, for example the sensors and the compute

## Autoware Index

The [Autoware Index](../installation/autoware/autoware-index.md) marks the entries that belong to a reference design. The `--reference-design` filter of `aw-index-cli` selects them.
