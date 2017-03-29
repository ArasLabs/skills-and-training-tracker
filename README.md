# Skills and Training Tracking System

This package is based on work done by Kostja Klein at Freudenberg FFD in Weinheim Germany. His solution was for the HR department to keep track of which employees had enrolled in which training classes, and included a provision for charge-back of training expenses to the employees department.

I removed the charge-back billing functions, translated to English, and added the concept of Job Roles.

A Job Role (e.g. CM Supervisor) requires certain skills. Skills are earned by attending Classes. Skills can have expirations (e.g Red Cross CPR must be renewed every 6 months).

The datamodel allows for a User to have multiple Job Roles (and hence skills training requirements). Each Job Role has 1 or more Skills required.

Some simple reports are included in the package, but this is the area (reporting and notifications) that needs the most work.

Some of this Packages elements are used to drive the www.aras.com/University/ web page for class display and enrollment.

**NOTE:** must be imported as Root instead of Admin, since it makes a modification to the core User itemType.

## History

This project and the following release notes have been migrated from the old Aras Projects page. Unlike community projects that have been migrated and archived, this project will be updated for compatibility with the latest release of Aras Innovator.

Release | Notes
--------|--------
[v2.1](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v2.1) | Fixed for Compatibilty with Aras Innovator 9.1.0 SP6
[v2.0](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v2.0) | Edited ItemTypes to allow Import into 9.1.0 SP6. Compatibility not fully tested.
[v1.1](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v1.1) | Problems with .mf file addressed.
[v1.0](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v1.0) | Initial release - packaged by Peter Schroer after using Kostja's package in the MyInnovator.com and Aras Univercity web site

#### Supported Aras Versions

Project | Aras
--------|------
[v2.1](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v2.1) | 9.1.0 SP6
[v2.0](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v2.0) | 9.1.0 SP6
[v1.1](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v1.1) | 8.1.1
[v1.0](https://github.com/ArasLabs/skills-and-training-tracker/releases/tag/v1.0) | 8.1.1

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Pre-requisites

1. Aras Innovator installed (version 11.0 SPx preferred)
2. Aras Package Import tool
3. **Skills** import packages

### Install Steps

1. Backup your database and store the BAK file in a safe place.
2. Open up the Aras Package Import tool.
3. Enter your login credentials and click **Login**
  * _Note: You must login as root for the package import to succeed!_
4. Enter the package name in the TargetRelease field.
  * Optional: Enter a description in the Description field.
5. Enter the path to your local `..\skills-and-training-tracker\Import\imports.mf` file in the Manifest File field.
6. Select **Skills** in the Available for Import field.
7. Select Type = **Merge** and Mode = **Thorough Mode**.
8. Click **Import** in the top left corner.
9. Close the Aras Package Import tool.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

For more information on contributing to this project, another Aras Labs project, or any Aras Community project, shoot us an email at araslabs@aras.com.

## Credits

Original Idea by Constantin Klein.
Project owned by Peter Schroer, Aras Corporation.

## License

Aras Labs projects are published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
