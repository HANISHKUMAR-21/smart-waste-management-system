# Solar Waste Segregation Dashboard

Spring Boot dashboard for monitoring solar-powered waste segregation and Arduino sensor records.

## Run locally

Requirements: Java 21+.

```powershell
.\mvnw.cmd spring-boot:run
```

The app starts at `http://localhost:8080`. It uses an embedded H2 database by default.
Make sure Java 21 or newer is available on `PATH` or configured through `JAVA_HOME`.

## MySQL

Set these environment variables to use MySQL:

```powershell
$env:DB_URL="jdbc:mysql://localhost:3306/solar_waste_db"
$env:DB_USERNAME="root"
$env:DB_PASSWORD="your-password"
$env:DB_DRIVER="com.mysql.cj.jdbc.Driver"
$env:DDL_AUTO="update"
.\mvnw.cmd spring-boot:run
```

## Arduino

The application tries to open `COM5` at startup. If unavailable, the dashboard remains available and logs that the port could not be opened.
