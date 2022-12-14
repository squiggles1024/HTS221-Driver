# HTS221

Simple HTS221 Temperature and Humidity Sensor Driver

To use, include .c and .h files in your project.

The user must:

1. Create a HTS221_Handle_t instance.
2. Create a HTS221_InitSettings_t struct with the desired device settings. It is recommended the user reference the data sheet for setting details.
3. Provide a Low Level IO Driver structure "HTS221_IO_t". At a minimum, this must include a "Read", "Write", and "GetTick" function. Unused function pointers should be set to NULL. If the user does not provide an IO Init function, the GPIO and communication bus must be initialized already.
4. Pass the created HTS221_Handle_t instance, HTS221_InitSettings_t instance, and HTS221_IO_t instance to the function "HTS221_Init" function.
