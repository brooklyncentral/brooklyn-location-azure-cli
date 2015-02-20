brooklyn-location-azure-cli
===

This project provides Brooklyn support for using Azure cloud, using the Azure CLI. 

NB:  This library is experimental and requires the CLI to be installed.
We hope as jclouds Azure support matures, that will replace this library!

### Prerequisites

The Azure CLI must be pre-installed and configured - see http://azure.microsoft.com/en-gb/documentation/articles/xplat-cli/

We recommend the "publish settings file" configuration.

### Build

To build, simply run `mvn clean install`.


### Installation

To make the Azure location available to your Brooklyn apps, add a maven dependency for this project to your Brooklyn project (built from the Brooklyn arhectype, for example). Alternatively build this project and add the jar to your `$BROOKLYN_HOME/lib/dropins` folder.


### Configuration

Below is an example location configuration (in YAML):

    location:
      azure:
        region: North Europe
        imageId: <image to create>
        azureBinaryLocation: /path/to/azure
        azureUser: <login name to create>
        azurePassword: <password to create>

This can also be configured in `~/.brooklyn/brooklyn.propeties`. For example:

    brooklyn.location.named.azure-europe=azure
    brooklyn.location.named.azure-europe.region=North Europe
    brooklyn.location.named.azure-europe.imageId=0b11de9248dd4d87b18621318e037d37__RightImage-CentOS-6.6-x64-v14.2
    brooklyn.location.named.azure-europe.azureBinaryLocation=/usr/local/bin/azure
    brooklyn.location.named.azure-europe.azureUser=brooklyn
    brooklyn.location.named.azure-europe.azurePassword=CorrectHorseBatteryStaple
