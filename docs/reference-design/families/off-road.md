# Off-road

The off-road family covers vehicles that drive on unpaved terrain without road infrastructure, for example racing, research, and education platforms.

| Field       | Value                                                                                                                |
| ----------- | -------------------------------------------------------------------------------------------------------------------- |
| Application | Driving on unpaved terrain without lanes, signs, or maps                                                             |
| Guideline   | [Off-road reference design guideline](https://autowarefoundation.github.io/autoware.orv-reference-design-docs/main/) |
| Status      | Proposed                                                                                                             |

## Off-road racer

The first reference design is a small off-road racer.

### Deployment profile

| Part                 | Target                                                                         |
| -------------------- | ------------------------------------------------------------------------------ |
| Vehicle platform     | A small off-road racer with cameras and an NVIDIA Jetson AGX Orin or Orin Nano |
| Operating conditions | Unpaved tracks, for example a pump track. The ODD is not specified yet.        |
| Use case             | Racing, research, and education                                                |

Machine learning vision models detect the drivable area and the route. The guideline uses NVIDIA Isaac Sim to simulate the off-road environment before tests on the vehicle.

### Variants

| Variant | Deployment profile                           | Reference software stack | Status   |
| ------- | -------------------------------------------- | ------------------------ | -------- |
| A       | Off-road racer platform and operating target | Not specified yet        | Proposed |

## Open items

- Specify the reference software stack and add it to [Reference software stacks](../software-stacks.md).
- Specify the ODD, the chassis, and the sensors. The sensor page of the guideline is a copy of the PoV guideline.
- Write the six blueprint sections. See the [reference design template](../template.md).
