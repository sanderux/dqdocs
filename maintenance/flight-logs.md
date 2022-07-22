# Flight logs

The DeltaQuad records on-board logs that contain vast amounts of information regarding the flights. These on-board logs are stored on the SD-Card and should be retrieved and processed after one or more flights.

Every DeltaQuad should have a well maintained logbook that keeps a record of every flight. In most cases when having your vehicle certified this is a requirement.

## Processing the on-board flight logs

On-board flight logs can be retrieved from the SD-Card in the flight controller. Remove the SD-Card and download the log files from the Log folder on the card. The logs will be stored in a subfolder that is named by the date of the flights. Logs can be uploaded to [DeltaQuad Flight Review](https://logs.deltaquad.com/) for an easy overview. Logs should also be stored locally as the DeltaQuad Flight Review server does not store logs indefinitely.

Logs can also be reviewed using the [Flightplot](https://pixhawk.org/dev/flightplot) application. This does require in-depth knowledge of the log format.

After retrieving the on-board flight logs remember to re-insert the SD-Card in the flight controller. As this can be easily overlooked it is recommended to store a spare SD-Card in your flight kit. Always use industrial temperature rated sd-cards.

## Maintaining a log book

For professional use and fleet management Vertical Technologies recommends the use of [AlarisPro](https://www.alarispro.com/). The DeltaQuad is a known vehicle in this system and all components and maintenance schedules are pre-configured.

For other, or self designed log books the following information should at least be present;

Per vehicle

* Serial number
* Total flight hours
* Last maintenance cycle
* Replaced components including replacement date

Per flight

* Vehicle serial number
* Date and time
* Flight time
* Link to the on-board log and/or flight review
* Operator
* Weather conditions / wind speed
* Flight notes, failures, damage and field replacements
