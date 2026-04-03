# Exploring_common_flutter_widget
Exploring Common Flutter Widgets: Lab Series This repository contains a collection of lab assignments focused on mastering Flutter's widget-based architecture. Each lab explores different categories of widgets, from basic structural components to complex interactive elements.

Lab 01: Structural & Basic Widgets
Objective: Understanding the foundation of a Flutter app using Scaffold, AppBar, Text, and Container.

Key Concepts: Widget properties (padding, margin, decoration), text styling, and basic app structure.

Widget Tree Highlights:

MaterialApp -> Scaffold -> Center -> Text

Lab 02: Multi-Child Layout Widgets
Objective: Organizing UI elements using Row and Column.

Key Concepts: MainAxisAlignment vs. CrossAxisAlignment, Expanded, and SizedBox for spacing.

Widget Tree Highlights:

Column -> [Row, Container, Expanded]

Lab 03: Assets & Interaction
Objective: Integrating local/network images and responding to user taps.

Key Concepts: Image.asset, Icon, and wrapping widgets in GestureDetector or InkWell.

Widget Tree Highlights:

GestureDetector -> Image

Lab 04: Input & Form Widgets
Objective: Building user input forms.

Key Concepts: TextField, ElevatedButton, and managing user input via controllers.

Widget Tree Highlights:

Form -> Padding -> Column -> [TextField, ElevatedButton]


Documentation (Visuals)
Every lab folder includes a /screenshots directory containing:

Running App: A real-time preview of the UI on an emulator or physical device.

Widget Tree: A visualization from the Flutter DevTools Inspector showing the hierarchy of nested widgets.

Tech Stack
Framework: Flutter (Latest Stable)

Language: Dart

Tools: VS Code / Android Studio, Git, flutter sdk

## Student Information

| Property | Details |
| :--- | :--- |
| **Name** | Marta Tegegne |
| **UGR Number** | ugr/4457/16 |
| **Section** | 1 |

**About .gitignore**
Each project folder includes a dedicated .gitignore file to ensure that auto-generated build files and binaries are excluded from the version control, keeping the repository lightweight and focused on source code.


Security Measures
To ensure code integrity and project security, the following measures have been implemented:

Access Control: Repository is set to restricted write access; only authorized contributors can merge code.

Branch Protection: The main branch requires a Pull Request and status checks before merging.

Secret Management: .gitignore is utilized to prevent sensitive build artifacts from being exposed.

Dependency Scanning: Dependabot is enabled to monitor for vulnerabilities in Flutter/Dart packages.
## flutter routing

This project demonstrates how to implement navigation in Flutter using the GoRouter package. It includes:

Basic navigation between screens
Passing path parameters (e.g., product ID)
Using query parameters (e.g., filters)
Clean and scalable routing setup
#### Features
Navigate from Home screen to Product Details
Dynamic route handling (/product/:id)
Query parameter support (?filter=popular)
Simple and maintainable routing structure

#### package
go_router package is used
## Flutter Routing Approaches
-Navigator 1.0 (Traditional Routing)
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => ProductDetailScreen()),
);
#### Pros
Simple and easy to learn
Built-in (no extra package)
Good for small apps
#### Cons
Hard to manage in large apps
No URL support (bad for web)
Difficult to handle deep linking

## Navigator 2.0 (Advanced / Declarative)

#### Pros
Full control over navigation
Supports web URLs and deep linking
Very powerful
#### Cons
Very complex
Too much boilerplate
Hard for beginners

## GoRouter (Modern & Recommended)
GoRoute(
  path: '/product/:id',
  builder: (context, state) => ProductDetailScreen(),
);
#### Pros
Simple and clean
Supports:
URL routing
deep linking
parameters
Less boilerplate than Navigator 2.0
Officially recommended by Flutter team
#### Cons
Requires external package
Slight learning curve

## Best Choice: GoRouter
.Combines simplicity (Navigator 1.0) + power (Navigator 2.0)
