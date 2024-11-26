# BookStore

## Now Upgraded to .NET 8.0

---

### How to Run the Project

1. **Clone the Repository**  
   Clone the project to your local machine using the following command:  
   
   git clone from: [over here](https://github.com/https://github.com/hsondz1910/DotNet-Assignment-10percent)


2. **Update Connection String**  
   Open the `appsettings.json` file and update the connection string to match your SQL Server configuration:  
   ```json
   "ConnectionStrings": {
     "conn": "data source=YOUR_SERVER_NAME;initial catalog=BookStore;integrated security=true;trust server certificate=true"
   }
   ```
   Replace `YOUR_SERVER_NAME` with the name of your SQL Server instance.
   
   *Trust the self-signed SSL certificate*
   If you need HTTPS for your project:
   Open a Command Prompt or PowerShell with Admin privileges.
   Run the following command:
   ``` bash
   dotnet dev-certs https --trust
   ```
   Once the command is run, the system will add the .NET self-signed certificate to the Trusted Root Certification Authorities.
   Restart the application and visit https://localhost:5000 again.

4. **Delete the Migrations Folder**  
   Navigate to the `Migrations` folder in the project and delete it.

5. **Run Migrations and Update Database**  
   Open **Visual Studio** and go to `Tools > NuGet Package Manager > Package Manager Console`.  
   Run the following commands in the console:
   ```bash
   add-migration init
   update-database
   ```

6. **Run the Project**  
   Once the above steps are completed, you can run the project using Visual Studio or `dotnet run`.

---

### Notes
- Ensure you have **.NET 8.0 SDK** installed on your system.
- Make sure your SQL Server is running and accessible.
- If you face issues with database connectivity, verify your connection string and server configuration.
