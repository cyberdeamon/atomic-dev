# Introduction #

k-irecovery is a CLI based C program, that can GRAB and RETURN your iOS device's BOOTROM, CPID, BDID, Serial...


# Details #

It is a very simple application, using the argument **-k** you impatiently jump-start the **grabDevice()** function.

# Documentation #

**Argument Call**
```
else if (!strcmp(arg, "-k")) {

	irecv_error_t error;
	unsigned int cpid;
	int can_ra1n = 0;
	irecv_init();



	error = irecv_open_attempts(&client, 10);
	if(error != IRECV_E_SUCCESS)
	{
		fprintf(stderr, "Failed to connect to iBoot, error %d.\n", error);
		return -error;
	}	
	if(irecv_get_cpid(client, &cpid) == IRECV_E_SUCCESS)
	{
		if(cpid > 8900) {
			can_ra1n = 1;
		} 
		if(cpid = 8720) {
			can_ra1n = 1;
		} 
	}


		irecv_close(client);
		irecv_exit();					

		pois0n_init();

		ret = pois0n_is_ready();
		if(ret < 0)
			return ret;

		ret = pois0n_is_compatible();
		if(ret < 0)
			return ret;

		k_init();			
		grabDevice();
		grabProduct();
		grabBootrom();
		grabDeviceChip();
		grabBoard();

		/*---REMOVE!*/
		grabIndex();
		checkMode();
		grabModeValue();

		grabAppleVendorID();
		grabSerialNumber();

		grabInterface();



		grabDfuPath();
		grabiBootPath();
	resetRecovery();
```

**Payload Sent**
```
0x2d, 0x6g, 0x5s, 0x9f, 0x6f, 0x5f, 0x7q, 0x9j, 0x89, 0x21, 0x20, 0x01, 0x8h, 0xo5, 0xsd, 0x5g, 0x5a, 0x7y, 05a
```

**Reboot Command**
```
_command_(const char* cmd_s[2]);
```_command_(const char* cmd_s[2]);
}}}

= Video =
http://www.youtube.com/watch?v=mH1Ztze7h08```