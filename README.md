# ATI
Utility tool for inspecting ATI F/T sensor data with a Q8-USB

## Usage

1. Place your calibration file (e.g. `FT06833.cal`) in the same directory as the application.
2. Provide the application with the serial number and the analog input channel numbers:

```shell
> ati.exe -s FT06833 -c 0,1,2,3,4,5
```
