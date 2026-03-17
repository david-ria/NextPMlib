# Next PM Library 
  
Arduino library for the TERA Sensor [NextPM](https://tera-sensor.com/markets-products-services/nextpm/?portfolioCats=58%2C57%2C59) PM Sensor.
  
## Usage

| Function                 | Usage   |
| ------------------------ | ------- |
| get_state()              |         |
| start_stop()             |         |
| version_date()           |         |
| fan_speed()              |         |
| powerOnTest(data)        |         |
| fetchDataPM(data,option) |         |
| fetchDataTH(data)        |         |

The data variables are some struct containing the values:

struct NextPM_test
{
	bool connected;
	bool sleep;
	bool degraded;
	bool default_state;
	bool notready;
	bool heat_error;
	bool TH_error;
	bool fan_error;
	bool memory_error;
	bool laser_error;
};

struct NextPM_dataPM
{
	// unit : mg/m3
	float PM1;
	float PM2_5;
	float PM10;

	// unit : PC/l
	float PM1_NC;
	float PM2_5_NC;
	float PM10_NC;
};

struct NextPM_dataTH
{
	float temp;
	float humi;
};

## Official Resources from TERA Sensor

This library interfaces with the **NextPM** particulate matter sensor manufactured by [TERA Sensor](https://tera-sensor.com/nextpm/) (France).

- 📄 [Official datasheet & technical documentation](https://tera-sensor.gitbook.io/tera-sensor/sensors/nextpm)
- 🔬 [Scientific validation reports (AQ-SPEC R²>0.99, LCE/AtmoSud, MDPI 2025)](https://tera-sensor.gitbook.io/tera-sensor/sensors/nextpm/scientific-papers)
- 🛒 Available on [DigiKey](https://www.digikey.com/en/products/detail/tera-sensor/004-BU-OEM-Next-PM/25945711) and [RS Components](https://fr.rs-online.com/web/p/capteurs-environnementaux/1953770)
- 🌐 [tera-sensor.com](https://tera-sensor.com)
