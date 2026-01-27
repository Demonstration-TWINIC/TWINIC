## Dataset Description

This directory contains sample trajectory data provided for illustrating the data format and signal characteristics used in the TWINIC project.
The data are organized by traversal paths, where each path includes multiple collections conducted at different times.

The dataset is intended as an **example dataset** for understanding the data structure and for demonstrating algorithmic behavior, rather than as a comprehensive benchmark.

---

## Directory Structure

For each traversal path, multiple sensing sessions are preserved:

```
Parking_Path_xx/
├── sensor_xxxx.csv
└── signal_xxxx.csv
```

Each `Parking_Path_xx` corresponds to an independent walking trajectory within the same parking environment.

---

## Sensor Data Format

### `sensor_xxxx.csv`

This file records motion and geomagnetic sensor readings collected during the traversal.

| Field | Description |
|------|-------------|
| Time | Timestamp of the measurement |
| Acc_X, Acc_Y, Acc_Z | Tri-axial accelerometer readings |
| Meg | Geomagnetic signal magnitude |
| Gyr_X, Gyr_Y, Gyr_Z | Tri-axial gyroscope readings |
| Ore | Device orientation or heading angle |

---

## Wireless Signal Data Format

### `signal_xxxx.csv`

This file records wireless signal measurements collected during the traversal.

| Field | Description |
|------|-------------|
| Time | Timestamp of the scan |
| Cell_Type | Cellular network type (e.g., LTE) |
| Cell_ID | Cellular cell identifier (anonymized) |
| Cell_RSSI | Cellular signal strength (dBm) |
| WiFi_MAC | MAC address of WiFi access point |
| WiFi_ID | Anonymized or logical WiFi identifier |
| WiFi_RSSI | WiFi signal strength (dBm) |

> Note: Sensitive identifiers such as `Cell_ID` and `WiFi_MAC` are anonymized
> or should be anonymized before public release.

---

## Data Collection

The trajectories were collected using a custom-developed smartphone sensing application that records synchronized inertial, geomagnetic, and wireless signals.
The application is not publicly released, as this repository focuses on illustrating the signal-space behavior and system-level results rather than data acquisition tooling.

To ensure data quality and consistency, the following guidelines were followed during data collection:

1. Avoid excessive device shaking or abrupt movements.
2. Avoid prolonged stationary periods during traversal.
3. Avoid repetitive back-and-forth walking along the same short segment.
4. Maintain a natural and continuous walking pace throughout the trajectory.

---

## Notes

- All data are collected using commodity smartphones.
- Absolute physical coordinates are not provided.
- The dataset is intended for research and algorithm evaluation purposes.
