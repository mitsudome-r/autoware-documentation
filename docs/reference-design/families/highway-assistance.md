# Highway assistance

The highway assistance family covers driver assistance on highway routes, in privately owned passenger vehicles.

| Field       | Value                                                                                                           |
| ----------- | --------------------------------------------------------------------------------------------------------------- |
| Application | Driver assistance on highway routes                                                                             |
| Guideline   | [PoV reference design guideline](https://autowarefoundation.github.io/autoware.pov-reference-design-docs/main/) |
| Status      | Proposed                                                                                                        |

## Vision Pilot highway assistance

The baseline reference design uses one front camera and the [Vision Pilot](../software-stacks.md#vision-pilot) stack.

### Deployment profile

| Part                 | Target                                                                                                               |
| -------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Vehicle platform     | A passenger vehicle with one forward-facing 8 MP RGB camera with a 120 degree horizontal field of view               |
| Operating conditions | Single-lane highways with clearly marked lane lines, fair weather and visibility, 0 to 70 mph, no construction zones |
| Use case             | SAE Level 2+ driver assistance. The driver monitors and supervises the system at all times.                          |

The target functions are:

- forward collision warning and automatic emergency braking
- lane departure warning and lane departure avoidance
- intelligent speed assist and traffic-aware adaptive cruise control
- lane keeping and road following

The full ODD is not specified yet.

### Variants

The PoV guideline plans more variants. Each adds sensors and has its own deployment profile.

| Variant           | Added sensors and data                                        | Automation target | Status   |
| ----------------- | ------------------------------------------------------------- | ----------------- | -------- |
| Vision Pilot      | One front camera                                              | Level 2+          | Proposed |
| Vision Pilot Plus | One 4D imaging radar and two corner radars                    | Level 3           | Planned  |
| Vision Pilot Pro  | Three front cameras and a standard 2D navigation map with GPS | Level 3           | Planned  |
| Vision Drive      | Short-wave and long-wave infrared cameras                     | Level 4           | Planned  |

The guideline gives the target GPU performance of each variant, from 50 TOPS to 1000 TOPS.

## Open items

- Rename the PoV guideline to the highway assistance reference design, and use the six blueprint sections. See the [reference design template](../template.md).
- Update the software section of the guideline from AutoSeg to AutoSteer, AutoSpeed, and AutoDrive.
- Specify the reference vehicle and complete the platform section.
- Record the evaluation results for one tested configuration.
