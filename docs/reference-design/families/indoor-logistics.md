# Indoor logistics

The indoor logistics family covers vehicles that move goods in GPS-denied, structured indoor areas, for example warehouses.

| Field       | Value                                                                                                                                    |
| ----------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Application | Goods transport in warehouses and other structured indoor areas                                                                          |
| Guideline   | [LSA reference design guideline, indoor ODD](https://autowarefoundation.github.io/LSA-reference-design-docs/main/odd-definition/indoor/) |
| Status      | Proposed                                                                                                                                 |

[:octicons-link-external-24: Read the detailed guideline](https://autowarefoundation.github.io/LSA-reference-design-docs/main/odd-definition/indoor/){ .md-button .md-button--primary }

## Warehouse vehicle

The first reference design is a vehicle for warehouse aisles.

### Deployment profile

| Part                 | Target                                                                                     |
| -------------------- | ------------------------------------------------------------------------------------------ |
| Vehicle platform     | A small vehicle with a wide field-of-view LiDAR, wide-angle and depth cameras, and no GNSS |
| Operating conditions | Indoor, structured, GPS-denied areas with narrow aisles, typically 5 to 10 km/h            |
| Use case             | Goods transport between fixed points                                                       |

The vehicle localizes with LiDAR SLAM and markers, for example AprilTags or reflectors. The [Indoor configuration](https://autowarefoundation.github.io/LSA-reference-design-docs/main/get-started/build-examples/) of the LSA guideline gives an example platform.

### Variants

| Variant | Deployment profile                              | Reference software stack                                                     | Status   |
| ------- | ----------------------------------------------- | ---------------------------------------------------------------------------- | -------- |
| A       | Warehouse vehicle platform and operating target | [Rule-based Planning](../software-stacks.md#rule-based-planning), to confirm | Proposed |

## Open items

- Confirm the reference software stack and the localization method.
- Complete the indoor ODD of the LSA guideline.
- Write the six blueprint sections. See the [reference design template](../template.md).
