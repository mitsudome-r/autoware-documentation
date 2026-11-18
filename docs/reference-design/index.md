# Reference design

An Autoware reference design is a complete system blueprint with reusable parts. It combines a deployment profile with a reference software stack:

- The **deployment profile** sets the target: the vehicle platform, the operating conditions, and the use case.
- The **reference software stack** supplies the software: the modules, the model versions, the parameters, and the interfaces.

In short, a reference design is a deployment profile plus a reference software stack.

A reference design is documented and versioned, so that others can reproduce and assess the system. Its status separates the intended capability from the demonstrated results.

{{ diagram("images/reference-design-concept.svg", "A deployment profile and a reference software stack make a reference design. A family groups related reference designs.") }}

To learn the terms, see [Reference design concepts](concepts.md). To write a reference design, use the [reference design template](template.md).

## Families

The catalog is organized by application. A family groups the reference designs of one application. Each reference design has a baseline and can have documented variants.

<div class="grid cards" markdown>

- **Low-speed shuttle**

  ***

  Campus and local passenger transport. The campus shuttle has variants with rule-based planning, a diffusion planner, and METEOR.

  [:octicons-arrow-right-24: Low-speed shuttle](families/low-speed-shuttle.md)

- **Highway assistance**

  ***

  Driver assistance on highway routes in passenger vehicles, with the camera-based Vision Pilot stack.

  [:octicons-arrow-right-24: Highway assistance](families/highway-assistance.md)

- **Urban robotaxi**

  ***

  Passenger transport in urban areas within a defined ODD, with the Fusion Pilot stack.

  [:octicons-arrow-right-24: Urban robotaxi](families/urban-robotaxi.md)

- **Indoor logistics**

  ***

  Goods transport in warehouses and other GPS-denied indoor areas.

  [:octicons-arrow-right-24: Indoor logistics](families/indoor-logistics.md)

- **Off-road**

  ***

  Driving on unpaved terrain without road infrastructure, for racing, research, and education.

  [:octicons-arrow-right-24: Off-road](families/off-road.md)

</div>

## Catalog

Each field of a catalog entry is independent: the family, the ODD, the platform, the sensors, the software, and the evaluation.

| Family             | Target ODD                                               | Platform          | Sensors                                            | Software                                                                  | Evaluation |
| ------------------ | -------------------------------------------------------- | ----------------- | -------------------------------------------------- | ------------------------------------------------------------------------- | ---------- |
| Low-speed shuttle  | Paved campus, daylight, dry, 15 km/h or less             | Shuttle           | LiDAR, cameras, GNSS/IMU                           | [Rule-based Planning](software-stacks.md#rule-based-planning)             | Proposed   |
| Low-speed shuttle  | Paved campus, daylight, dry, 15 km/h or less             | Shuttle           | LiDAR, cameras, GNSS/IMU                           | [Diffusion Planning](software-stacks.md#diffusion-planning)               | Proposed   |
| Low-speed shuttle  | Campus target. The model requirements are not confirmed. | Shuttle           | Not confirmed                                      | [Meteor-based](software-stacks.md#meteor-based)                           | Proposed   |
| Highway assistance | Highway target. The ODD is not specified.                | Passenger vehicle | Camera-based. The inputs are not specified.        | [Vision Pilot](software-stacks.md#vision-pilot)                           | Proposed   |
| Urban robotaxi     | Urban target. The ODD is not specified.                  | Passenger vehicle | Cameras and LiDARs. The details are not specified. | [Fusion Pilot](software-stacks.md#fusion-pilot)                           | Proposed   |
| Indoor logistics   | Indoor, GPS-denied, 5 to 10 km/h                         | Small vehicle     | Wide field-of-view LiDAR, cameras                  | [Rule-based Planning](software-stacks.md#rule-based-planning), to confirm | Proposed   |
| Off-road           | Unpaved tracks. The ODD is not specified.                | Small racer       | Cameras                                            | Not specified                                                             | Proposed   |

The operating targets, the compatibility, and the evaluation are not established yet.

## Reference software stacks

Autoware publishes and maintains the reference software stacks as recommended baselines. One stack can serve the deployment profiles of many reference designs. See [Reference software stacks](software-stacks.md).

The [Autoware Index](../installation/autoware/autoware-index.md) at [index.autoware.org](https://index.autoware.org) marks the entries that belong to a reference design.

## Example builds

These community builds use Autoware. They are not reference designs, because they do not define a deployment profile, a reference software stack, and an evaluation. They are good examples for racing, education, and prototypes.

- [RoboRacer](get-started/RoboRacer/index.md): a 1/10 scale platform for racing and education
- [Go-Kart](get-started/GoKart/index.md): an electric go-kart for racing and development
- [AutoSDV](get-started/AutoSDV/index.md): an affordable 1/10 scale platform for education and research
- [Autoware delivery vehicle](get-started/Delivery/index.md): a concept for a delivery vehicle on a private campus
- [ITRI Bus](itri-bus/index.md): a bus for public roads from the Bus ODD project

To compare them, see [Find your reference design](get-started/find-your-reference-design.md).

## Reference hardware

[:fa-cl-s fa-circle-arrow-right: Reference Hardware Section](reference-hw/index.md){ .md-button }
