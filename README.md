# M2L - Maison des Ligues Event Management System

A Windows Forms desktop application for managing events at the "Maison des Ligues" (House of Leagues). This school project demonstrates the implementation of MVC architecture with a Data Access Object (DAO) pattern in C# .NET Framework.

## 📋 Features

- **🔐 Authentication System** - Secure login functionality for administrators
- **🎪 Workshop Management (Ateliers)** - Create, modify, and delete workshops with themes, capacity, and scheduling
- **👥 Participant Management** - Track participants and their types
- **🏨 Hotel Management** - Manage hotel accommodations for event attendees
- **🎯 Stand Allocation** - Visual stand booking system with availability indicators and partner assignment

## 🛠️ Technology Stack

- **Language:** C# (.NET Framework 4.6)
- **UI Framework:** Windows Forms
- **UI Libraries:**
  - [Bunifu UI v1.52](https://bunifuframework.com/) - Modern flat UI components
  - [MaterialSkin](https://github.com/IgnaceMaes/MaterialSkin) - Material Design styling
- **Database:** SQL Server (LocalDB)
- **IDE:** Visual Studio 2019+

## 🏗️ Architecture

The project follows the **MVC (Model-View-Controller)** pattern with a **DAO (Data Access Object)** layer:

```
Main/
├── LogicLayer/          # Models (Business Logic)
│   ├── Atelier.cs       # Workshop entity
│   ├── Hotel.cs         # Hotel entity
│   ├── Participant.cs   # Participant entity
│   ├── Partenaire.cs    # Partner entity
│   ├── Reservation.cs   # Reservation entity
│   ├── Stands.cs        # Stand entity
│   └── Theme.cs         # Theme entity
│
├── DAO/                 # Data Access Objects
│   ├── DAOFactory.cs    # Database connection factory
│   ├── DAOAtelier.cs    # Workshop data operations
│   ├── DAOAuth.cs       # Authentication data operations
│   ├── DAOHotel.cs      # Hotel data operations
│   ├── DAOParticipants.cs
│   ├── DAOPartenaires.cs
│   ├── DAOReservation.cs
│   ├── DAOStands.cs     # Stand data operations
│   └── DAOTheme.cs      # Theme data operations
│
├── Forms/               # Views (Windows Forms)
│   ├── authentication.cs        # Login form
│   ├── Form1.cs                 # Main application form
│   ├── m2lAteliers.cs           # Workshop management view
│   ├── m2lHotel.cs              # Hotel management view
│   ├── m2lParticipants.cs       # Participant management view
│   ├── m2lStands.cs             # Stand management view
│   ├── AjouterAtelier.cs        # Add workshop dialog
│   ├── ModifierAtelierModal.cs  # Edit workshop dialog
│   ├── standAllocation.cs       # Stand allocation dialog
│   └── atelierUserManaging.cs   # Workshop user management
│
└── Resources/           # Application resources (icons, images)
```

## 📦 Prerequisites

- **Windows 10/11**
- **Visual Studio 2019** or later with:
  - .NET desktop development workload
  - SQL Server Data Tools
- **SQL Server LocalDB** (included with Visual Studio)

## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/faycalsaid/school-project-c-sharp-mvc-app.git
   cd school-project-c-sharp-mvc-app
   ```

2. **Open the solution:**
   - Open `Main/Main.sln` in Visual Studio

3. **Restore NuGet packages:**
   - Right-click on the solution in Solution Explorer
   - Select "Restore NuGet Packages"

4. **Set up the database:**
   - Create a new LocalDB database named `M2L_TeamB`
   - Configure the connection string in `DAO/DAOFactory.cs` if needed:
     ```csharp
     "Data Source=(localdb)\\MyInstance; Initial Catalog=M2L_TeamB; User Id=root; Password=root;"
     ```

5. **Build and run:**
   - Press `F5` or click "Start" in Visual Studio

## 🗄️ Database Configuration

The application uses SQL Server LocalDB. To configure your own database:

1. Update the connection string in `Main/Main/DAO/DAOFactory.cs`
2. Create the following tables:
   - `Atelier` - Workshops
   - `Theme` - Workshop themes
   - `Participant` - Event participants
   - `TypeParticipant` - Participant categories
   - `Hotel` - Hotel information
   - `Reservation` - Hotel reservations
   - `Stands` - Event stands
   - `Partenaire` - Partners/Exhibitors
   - `Users` - Authentication users

## 📁 Project Structure

```
school-project-c-sharp-mvc-app/
├── Main/
│   ├── Main.sln           # Visual Studio solution file
│   └── Main/
│       ├── Main.csproj    # Project file
│       ├── Program.cs     # Application entry point
│       ├── App.config     # Application configuration
│       ├── DAO/           # Data access layer
│       ├── LogicLayer/    # Business logic/models
│       ├── Properties/    # Assembly information
│       ├── Resources/     # UI resources (DLLs, images)
│       └── *.cs           # Form files
├── assets/
│   └── icons/             # Application icons
├── LICENSE                # MIT License
└── README.md              # This file
```

## 📸 Screenshots

*Add screenshots of your application here*

<!-- Example:
![Login Screen](assets/screenshots/login.png)
![Main Dashboard](assets/screenshots/dashboard.png)
![Stand Management](assets/screenshots/stands.png)
-->

## 🤝 Contributing

This is a school project, but suggestions and improvements are welcome!

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Fayçal Saïd**

---

*This project was created as part of a school curriculum to demonstrate proficiency in C#, .NET Framework, Windows Forms development, and software architecture patterns.*
