# Low-speed shuttle

The low-speed shuttle family covers campus and local passenger transport at low speed.

| Field       | Value                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------ |
| Application | Campus and local passenger transport                                                                   |
| Guideline   | [LSA reference design guideline](https://autowarefoundation.github.io/LSA-reference-design-docs/main/) |
| Status      | Proposed                                                                                               |

[:octicons-link-external-24: Read the detailed guideline](https://autowarefoundation.github.io/LSA-reference-design-docs/main/){ .md-button .md-button--primary }

## Campus shuttle

The campus shuttle is the first reference design of this family.

### Deployment profile

| Part                 | Target                                                      |
| -------------------- | ----------------------------------------------------------- |
| Vehicle platform     | A shuttle with LiDARs, cameras, and a GNSS/IMU              |
| Operating conditions | Paved campus routes, daylight, dry weather, 15 km/h or less |
| Use case             | Passenger transport on fixed campus routes                  |

The [Campus configuration](https://autowarefoundation.github.io/LSA-reference-design-docs/main/get-started/build-examples/) of the LSA guideline gives an example platform and its performance targets.

### Variants

One deployment profile supports several defined software configurations.

| Variant | Deployment profile                                                                            | Reference software stack                                         | Status   |
| ------- | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | -------- |
| A       | Campus shuttle platform and operating target                                                  | [Rule-based Planning](../software-stacks.md#rule-based-planning) | Proposed |
| B       | Campus shuttle platform and operating target                                                  | [Diffusion Planning](../software-stacks.md#diffusion-planning)   | Proposed |
| C       | Campus shuttle platform and operating target, if it meets the platform requirements of METEOR | [Meteor-based](../software-stacks.md#meteor-based)               | Proposed |
| D       | Campus shuttle with cameras and radars                                                        | Camera and radar perception with rule-based planning             | Proposed |

The sensor requirements of variant C are not confirmed yet.

## Related deployments

These deployments use a campus shuttle with Autoware. They are not evaluated as variants of this reference design.

- [TalTech iseAuto](../get-started/find-your-reference-design.md#taltech-iseauto)
- [NC A&T Aggie Auto](../get-started/find-your-reference-design.md#nc-at-aggie-auto)

## Open items

- Write the six blueprint sections for variant A. See the [reference design template](../template.md).
- Specify the manifests of the stacks of variants A to D.
- Move the indoor configurations of the LSA guideline to the [indoor logistics](indoor-logistics.md) family.
