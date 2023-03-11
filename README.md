# service-registry

- It's a practice project to demonstrate interaction between several microservices.
- It consists of following projects

1. service-registry: https://github.com/goutam1997/service-registry
2. ui-service: https://github.com/goutam1997/ui-service
3. applicant-service: https://github.com/goutam1997/applicant-service
4. department-service: https://github.com/goutam1997/department-service
5. api-gateway: https://github.com/goutam1997/api-gateway

#Main Components used to build these projects
#Eureka Service Registry
#Feign Clients
#Api Gateway
#H2 Database

- Flow starts at `ui-service`.
- GET call from ui-service fetches applicants list from `applicant-service`.
- Ui-Service interacts with applicant-service by the help of `Feign Client` and `Service Registry`.
- Applicant-Service in turn calls `department-service` to insert departments.
- Department-Service uses in-memory `h2-database` to store applicantName and departmentName.
- Ui-Service can again call department-service to view departments info.