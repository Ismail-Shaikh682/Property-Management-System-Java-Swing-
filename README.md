🖥️ Current Output

The application was compiled and launched successfully in a Java 21 environment.

Main screen



Properties menu



Add Property screen



✅ Features Verified Working

The following parts were checked against the supplied source code and runtime environment:

Java/NetBeans project builds successfully

Apache Ant build completed with BUILD SUCCESSFUL.

19 Java source files compiled successfully.

Main Swing GUI launches

HomeScreenGUI opens successfully without a startup exception.

Main menu bar is visible.

Main navigation menus are present

File

Landlords

Properties

Tenants

Rentals

Help

Property Management UI

Record New Property window opens successfully.

Property entry fields are visible.

County dropdown is available.

Add Property and Cancel controls are present.

Landlord/tenant/property model classes

The supplied test-driver classes for Landlord, Person, Property, and Tenant execute successfully with exit code 0.

Constructors, getters, setters, and string output were exercised by those test drivers.

Local serialized data structure

The project includes local .data files for landlords, properties, tenants, and rentals.

Save/load helper code is included in the project.

⚠️ Known Issues / Incomplete Features

The project is not fully feature-complete in its current state.

Search Property is not implemented

The Search For Property menu item currently only prints:

Search For Property Clicked

and does not perform a search operation.

Search Rental is not implemented

The Search For Rental menu item currently only prints:

Search For Rental Clicked

and does not perform a search operation.

Runnable JAR manifest

The generated dist/Property_Rental.jar was created successfully, but its manifest does not contain a Main-Class entry. Therefore, the JAR should currently be launched from the project/classes or through NetBeans unless the manifest is configured.

Some GUI code needs cleanup

There are additional implementation issues in the current source, including fragile dialog handling and some menu/state logic that should be reviewed before production deployment.

Relative file paths

The application uses relative paths such as:

images/PropertyManagement.jpg
files/landlords.data
files/property.data

Run the program from the project root so these resources can be found correctly.

🛠️ Technology Stack

Language: Java

GUI: Java Swing

Build: Apache Ant

IDE Project: NetBeans

Persistence: Java object serialization (.data files)

📁 Project Structure

Property-Management-System-master/
├── build.xml
├── manifest.mf
├── nbproject/
├── src/
│   ├── HomeScreenGUI.java
│   ├── Landlord.java
│   ├── Property.java
│   ├── Person.java
│   ├── Tenant.java
│   ├── Rental.java
│   ├── LeaseProperty.java
│   ├── PropertyRent.java
│   ├── RegisterLandlordGUI.java
│   ├── RegisterNewTenantGUI.java
│   ├── RecordNewPropertyGUI.java
│   ├── AmendLandlordGUI.java
│   ├── AmendTenantGUI.java
│   └── ...test / data utility classes
├── images/
├── files/
└── terms-and-condition.pdf

▶️ How to Run in NetBeans

Open NetBeans.

Choose File → Open Project.

Select the Property-Management-System-master directory.

Build the project.

Run HomeScreenGUI.java.

▶️ How to Build with Ant

From the project root:

ant clean jar

A successful build creates:

dist/Property_Rental.jar

🧪 Verification Performed

The current project was checked with:

ant clean jar
ant test

The Java model test-driver classes were also executed successfully:

LandlordTest
PersonTest
PropertyTest
TenantTest

The main Swing application was launched and visually verified.
