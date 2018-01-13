# FRC Java IntelliJ Boilerplate
A template project for creating WPILib robot deployment code in IntelliJ.

## Installation
1. Download __wpilib__ to your home directory.
2. Clone this repository to a desired destination:
```
git clone https://github.com/Team334/frc-intellij.git
```
3. Open the cloned repository (*frc-intellij*) in IntelliJ with ```File > Open```.
4. To rename the project, right click on the folder and select ```Refactor > Rename```.
5. Change the package name to match your team number. Again use ```Refactor > Rename```.
```
org.us.first.frc.team334.robot → org.us.first.frc.team###.robot
```
6. Hit the green play button to deploy.

## Troubleshooting
— If the __wpilib__ library isn't included in your project, you can manually add its *jar* files:
1. Go to: ```File > Project Structure > Project Settings > Libraries```.
2. Add the library by pressing the __"+"__ button.
3. Navigate to ```wpilib/java/current/lib```.
4. Select the __wpilib__ jar files you want and add them. Don't forget to Apply the changes.
> Note: The __WPIib.jar__ is necessary for all the other *.jar*s you may want to add.

<br>

— If IntelliJ crashes while deploying, make sure you have the following files and folders in your project:
- ```build.properties```
- ```build.xml```
- ```sysProps.xml```
- ```/out```

If you don't, reinstall the project and follow the above instructions carefully.
You can also create the *out* folder by simply running the project and then force quitting IntelliJ and restart it. The created *out* folder should then appear when reopened.

<br>

— If you can't run the project, you need to create a new Ant Target.
1. Start by opening the Ant Build window ```View > Tool Windows > Ant Build```.
2. Click the "+" and add the __```build.xml```__ from this repo. "FRC Deployment" should appear in the Ant Build list.
3. Edit Configurations (button show in image below).

![Edit Configurations](/docs/edit-config.png)

4. Add a new *Ant Target* by clicking the __"+"__.
5. Give it a new name and browse for *deploy* in the Target name section.
6. Apply, and hit the green play button to deploy.

<br>
*If you find any other errors, please open a new issue on this repo that clearly explains your problem.* 
