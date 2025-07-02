# Salesforce Programmable Wallets

![](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/documentation-and-images/Web3-wallet-for-Salesforce-logo.png)

Programmable Wallets for Salesforce, powered by Circle Programmable Wallets, is an open source solution built on Circle Programmable Wallet technology to operating 100% within the Salesforce Ecosystem.

Key management is abstracted as Developer Managed Wallets, using Salesforce permissions to manage wallet safety. The company will be able to grant read, write, and execute permissions on the Web3 assets without leaving the environment they are comfortable with.

## Requirements

This is a basic demonstration of a Salesforce DX Project. The following Salesforce developer tools are prerequisites to install and set up Salesforce Programmable Wallets from this repository.

* **Salesforce DX Project Setup Information:** Download the [SF CLI tools](https://developer.salesforce.com/tools/salesforcecli), and use them to deploy to a Developer Edition Scratch Org.

* **Salesforce Developer Edition:** You can get a free Salesforce Developer Edition account from Salesforce. Sign up at:
https://developer.salesforce.com/signup


## Installation Instructions / How to Test the App

1. Clone the repository. `git clone https://github.com/MuKnSys/salesforce-programmable-wallets.git`
1. Change directory to the cloned repository. `cd salesforce-programmable-wallets`
1. Checkout the main branch.
1. Log into the Dev Hub Org by running
   `sf org login web --set-default-dev-hub --alias DevHub --instance-url https://login.salesforce.com`
   and entering your username and password.
1. Create a Scratch Org by running
   `sf org create scratch -f ./config/project-scratch-def.json -a dev -d -y 30`.
   - The `-f` flag is a path to config file (no need to change it).
   - The `-a` flag is an alias of the scratch org, if you create multiple
     scratch orgs you can give them unique aliases to easier refer to them.
   - The `-d` flag marks the newly created scratch org as default. If you don't
     mark it as default you will have to reference it by username or alias, or
     you will have to use `sf config set target-org YourAliasOrUsername` to set
     is as default.
   - The `-y` flag sets the number of days before the org expires.
   - Use the `-h` flag for help.
   - For more details:
     [developer docs scratch orgs create](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_scratch_orgs_create.htm).
1. Push the code to the Scratch Org: `sf project deploy start`.
1. Connect to the Salesforce Scratch Org: `sf org open`.

### Required Permission Set and Next Steps in the Setup Process

1. Assign permission set: `Programmable Wallets Admin` to your user
1. Use App Launcher to open `Programmable Wallets Setup`.
1. Please perform all the setup steps.


## Status of Project

### Milestone 1 - Project Setup

The initial Setup App and Screen is built. It allows you to connect to the Programmable Wallet system.

![](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/documentation-and-images/screenshot-setup.png)

This Open Source project requires you to register a developer key. This will be clarified in Milestone 3 as we prepare for final release. We are able to connect to the developer account. All "scaffolding is done."

For an explanation of the screen, please view [Milestone 1 Explainer Video](https://youtu.be/XJlX5Affdg8).

### Milestone 2 - Wallet Sets, Wallets, etc.

Milestone 2 demostrates the creation of Wallet Sets, Wallets of both types, and them showing up on the Circle Console. Milestone 3 was created contemporanously to Milestone 2.

![](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/documentation-and-images/screenshot-wallet-sets-with-wallets.jpg)

To utilize the Wallet Sets and Wallets, follow the setup steps below (Milestone 3) to create and register your API key.

1. Set up the API Key and Cypher Text (Milestone 3).
2. Launch Programmable Wallets for Salesforce in the App Switcher.
3. Create a New Wallet Set (name it, hit create).
4. Create one or more new Wallets in the Wallet Set.
5. Verify your Wallet on the [Circle Console Developer Controlled Wallets](https://console.circle.com/wallets/dev/wallets).

To see these features, watch [Milestone 2 during Milestone 2/3 Demo Video](https://youtu.be/4BBZACRtaew?si=BNENamc_rpDT1pKC&t=108).

### Milestone 3 - API Key, Cypher Text Creation and Storage

This Open Source Project now has custom Lightning Web Components to run the JavaScript necessary for registration.

![](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/documentation-and-images/screenshot-configuration-data.jpg)

1. Create a Circle Developer Account and Login [Circle Console](https://console.circle.com/).
2. Check your email to confirm and complete the account.
3. Grant your user the Permission Set, "Programmable Wallets Admin".
  1. Click the Gear for Setup.
  2. Quick Find "Users".
  3. Click on your user and scroll down to Permission Sets.
  4. Edit Assignments, and give yourself the [Programmable Wallets Admin permission](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/documentation-and-images/screenshot-permission-set.jpg).
4. In Salesforce Programmable Wallet Setup, Start the Configuration Process
5. Create an API Key on the [API & Client Keys of the Circle Console](https://console.circle.com/api-keys).
6. Register the Cypher Text on the [Circle Console Entity Secret Page](https://console.circle.com/wallets/dev/configurator/entity-secret).
7. Follow the Step by Step Creation Process to generate the Wallets (above).

Note: There is no supported way to copy the Cypher Text except via the NodeJS or Python SDKs. Therefore you must copy and paste it into the console.

[Milestone 2 and 3 Demo Video](https://youtu.be/4BBZACRtaew)


## Submitting changes to GitHub

1. Create a feature / change branch - you will need to fork the project.
1. Pull changes from Salesforce `sf project retrieve start`.
1. Push changes to GitHub.
1. Create a pull request.


## Additional Resources

-   [Salesforce Extensions Documentation](https://developer.salesforce.com/tools/vscode/)
-   [Salesforce CLI Setup Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_setup.meta/sfdx_setup/sfdx_setup_intro.htm)
-   [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_intro.htm)
-   [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)
-   [Salesforce DX Project Configuration](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/sfdx_dev_ws_config.htm)


## Copyright and License

Copyright 2024 Web3 Enabler, Inc. Web3 Wallet for Salesforce is distributed under the GPL licence, version 3.0. For more information, see the [LICENSE file](https://github.com/MuKnSys/web3-wallet-for-salesforce/blob/main/LICENSE).
