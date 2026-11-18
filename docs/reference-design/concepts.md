# Reference design concepts

This page defines the terms that the reference design pages use.

## Reference design

An Autoware reference design is a complete system blueprint with reusable parts. It combines two parts:

- A [deployment profile](#deployment-profile) sets the target: the vehicle, the operating conditions, and the use case.
- A [reference software stack](#reference-software-stack) supplies the software.

In short, a reference design is a deployment profile plus a reference software stack.

A reference design is documented and versioned. Thus, others can reproduce and assess the system.

{{ diagram("images/reference-design-concept.svg", "A deployment profile and a reference software stack make a reference design. A family groups related reference designs.") }}

## Deployment profile

A deployment profile describes the intended application and the operating conditions for a specified vehicle and hardware configuration. It has three parts:

| Part                 | Contents                                                                      |
| -------------------- | ----------------------------------------------------------------------------- |
| Vehicle platform     | The vehicle, the sensors, the compute, the actuation, and the interfaces.     |
| Operating conditions | The roads, the speed, the weather, the lighting, and other ODD boundaries.    |
| Use case             | The driving functions and the responsibilities of the driver or the operator. |

The profile states the target. The reference design defines its ODD and records what the evaluation supports. Use the [ASAM OpenODD](https://www.asam.net/standards/detail/openodd/) terms for the ODD.

For example, a campus shuttle profile has LiDARs, cameras, and a GNSS/IMU on a specified vehicle and compute. It drives on paved campus routes, in daylight and dry weather, at 15 km/h or less.

## Reference software stack

A reference software stack is a software configuration that Autoware publishes and maintains as a recommended baseline. Its name resolves to one configuration:

- the modules
- the model versions
- the parameters
- the interfaces
- the platform requirements

One stack can serve many deployment profiles, if the requirements of the stack fit each profile. One profile can also have many stacks. For the list of stacks, see [Reference software stacks](software-stacks.md).

## Family

A family groups the reference designs of one application, for example a low-speed shuttle. The catalog is organized by family. Each reference design in a family has a baseline and can have documented variants.

## Variant

A variant is one defined system configuration of a reference design. Variants of the same design can differ in the software stack, the sensors, or the operating target. For example, the campus shuttle has variants with rule-based planning and with a diffusion planner.

Evidence belongs to one defined configuration. Each variant records its version, its integration requirements, and its evaluation scope. A change to the hardware, the software, or the operating conditions requires an assessment of the affected evidence.

## Status

A reference design can start as a draft. Its status must separate the intended capability from the demonstrated results.

| Status       | Meaning                                                                                       |
| ------------ | --------------------------------------------------------------------------------------------- |
| Planned      | The variant is on the roadmap. Its deployment profile and stack are not defined yet.          |
| Proposed     | The family, the target ODD, and the stack are named. The details are not specified yet.       |
| Draft        | The blueprint has all six sections, but the evaluation results are not complete.              |
| Demonstrated | The evaluation results of the defined configuration are recorded, with the known limitations. |

## Blueprint contents

Each reference design documents the same six sections. The [reference design template](template.md) describes them.

| Section          | Contents                                                                                    |
| ---------------- | ------------------------------------------------------------------------------------------- |
| Purpose          | The driving functions, the use case, the automation target, and the human responsibilities. |
| Operating domain | The conditions, the boundaries, the assumptions, and the exclusions.                        |
| Platform         | The vehicle, the sensors, the compute, the actuation, and the interfaces.                   |
| Software         | The selected modules, models, versions, parameters, and dependencies.                       |
| Integration      | The calibration, the timing, the maps, the resources, and the deployment instructions.      |
| Evaluation       | The criteria, the tested configurations, the results, and the known limitations.            |
