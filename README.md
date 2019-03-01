# MMM-MotionDetector

## Installation

Just clone the module into your MagicMirror modules folder:

```
git clone https://github.com/rejas/MMM-MotionDetector.git
```

## Requirements

Accessing your (web)cam requires to have the client run on localhost or a HTTPS host (due to new requirements in Chrome for getUserMedia). The default value in your MagicMirror config.js is already `localhost` so most users shouldn't be affected.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
	{
		module: "MMM-MotionDetector",
		position: "top_left",	// Optional. This can be any of the regions. Displays debug informations.
		config: {
			// The config property is optional.
			// See 'Configuration options' for more information.
		}
	}
]
````

## Configuration options

The following properties can be configured:

| Option                       | Description
| ---------------------------- | -----------
| `captureIntervalTime`        | Time in ms between capturing images for detection<br><br>**Default value:** `1000`|
| `scoreThreshold`             | Threshold minimum for an image to be considered significant<br><br>**Default value:** `20`|
| `timeout`                    | Time in ms after which monitor is turned off when no motion is detected<br><br>**Default value:** `120000`|

#### Default value:

````javascript
config: {
    captureIntervalTime: 1000,
    scoreThreshold: 20,
    timeout: 120000
}
````

## Changelog

### [1.2.0] - 2019-03-01

- Add DOM for displaying basic debug information on the MagicMirror when a position is specified
- Updated documentation

### [1.1.0] - 2018-11-01

- Switch from tvservice to vgcencmd. Module can now be used with vc4-kms-v3d and vc4-fkms-v3d drivers.

### [1.0.0] - 2018-07-20

- Initial release
