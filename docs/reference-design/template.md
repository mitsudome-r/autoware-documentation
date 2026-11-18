# Reference design template

Use this template for each reference design. The guideline of each family follows it. One template makes the designs easy to compare. For the terms, see [Reference design concepts](concepts.md).

## Header

Start the document with a short header:

| Field                    | Example                                          |
| ------------------------ | ------------------------------------------------ |
| Family                   | Low-speed shuttle                                |
| Reference design         | Campus shuttle                                   |
| Variant                  | A: rule-based planning                           |
| Deployment profile       | Campus shuttle platform and operating target     |
| Reference software stack | Rule-based Planning, with its version            |
| Status                   | Proposed, Draft, or Demonstrated                 |
| Version                  | The version of this reference design             |
| Maintainers              | The people or the working group that maintain it |

## 1. Purpose

- The use case.
- The driving functions.
- The automation target, for example SAE Level 2 or Level 4.
- The responsibilities of the driver, the operator, or the remote operator.

## 2. Operating domain

Use the [ASAM OpenODD](https://www.asam.net/standards/detail/openodd/) terms.

- The conditions: the road types, the speed range, the weather, and the lighting.
- The boundaries: what makes the system leave its ODD, and what it does then.
- The assumptions, for example the map, the infrastructure, or the other road users.
- The exclusions: the conditions that the design does not support.

## 3. Platform

- The vehicle or the chassis, with its main dimensions.
- The sensors: the type, the model, the count, the position, and the field of view.
- The compute: the ECU, the CPU, the GPU or the accelerator, and the required performance.
- The actuation: the drive-by-wire system and its interface.
- The interfaces between the platform and Autoware.

For candidate parts, see [Reference HW](reference-hw/index.md).

## 4. Software

- The reference software stack and its version. See [Reference software stacks](software-stacks.md).
- The modules and the models, with their versions.
- The parameters that differ from the defaults of the stack.
- The dependencies, for example the ROS 2 distribution, the middleware, and the GPU runtime.

## 5. Integration

- The sensor calibration.
- The time synchronization and the timing budget.
- The maps: the type, the format, and how to make them.
- The resources: the CPU, the GPU, the memory, and the power.
- The deployment instructions, from a clean ECU to a running system.

## 6. Evaluation

- The criteria and the metrics.
- The tested configurations: the exact profile, the stack, and the versions.
- The results, with the date and the test environment.
- The known limitations.

Keep the intended capability and the demonstrated results apart. A result is valid only for the configuration that was tested.
