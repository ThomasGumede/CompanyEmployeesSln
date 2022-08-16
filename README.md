# Company Employees API

Company Employees API is web application api for storing company employees.

## Development Environment

- Linux Mint 20 
- VS Code

## Features

- GET/POST/DELETE/PUT/PATCH/HEAD/OPTION requests
- Paging, Sorting, Filtering, Searching, DataShaping, Caching response, Visioning Api, Rate limiter/throttling and HATEOAS
- User ragistration, sign in/up
- File logging using NLog
- 

## Libraries, Development Stack and Database Used

- asp.net core 6 Web API
- Jwt and Asp.net core 6 identity
- PostgresQl

## Documentation

- Update ConnectionString
- cd CompanyEmployees && run ```dotnet restore```
- run ```dotnet run```
- visit https://localhost:7072/swagger/index.html for swagger Doc

### Access Api Root

- add ```application/vnd.codemaze.apiroot+json``` to the Accept Header
- visit /api

### filtering

- visit /api/companies/{companyID}/employees?minAge={int:value}&maxAge={int:value}

### paging

- visit /api/api/companies/{companyID}/employees?pageNumber={int:value}&pageSize={int:value}

### searching

- visit /api/api/companies/{companyID}/employees?searchTerm={str:value}

### sorting

- visit /api/api/companies/{companyID}/employees?orderBy=name,age desc

### Data Shaping

- visit /api/api/companies/{companyID}/employees?/fields={fields you want}

### Do it all

- visit /api/companies/{companyID}/employees?pageNumber=1&pageSize=4&minAge=26&maxAge=32&searchTerm=A&orderBy=name,desc&fields=name,age

### Access Api Root

- add ```application/vnd.codemaze.hateoas+json``` to the Accept Header
- visit /api/companies/{companyID}/employees?pageNumber=1&pageSize=4&minAge=26&maxAge=32&searchTerm=A&orderBy=name,desc&fields=name,age