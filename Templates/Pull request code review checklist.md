### Review Before Submitting
- [ ] your code builds clean without any errors or warnings
- [ ] PR is small enough to be effectively reviewed (less than 200-400 lines of reviewable code)
- [ ] assign the necessary reviewers to the PR
- [ ] assign corresponding stories, activities, or tickets
- [ ] attach screenshots of developed UI

### Testing
- [ ] appropriate unit tests were created with the code
- [ ] appropriate integration tests were added if crossing services
- [ ] appropriate UI test were created where needed
- [ ] code coverage was maintained
- [ ] all tests pass

### Architecture
- [ ] new services have not been added that weren't in the architecture
- [ ] functionality added to existing services belongs in that service
- [ ] there are no references that contradict architecture guidelines
- [ ] business logic is being properly encapsulated and tested
- [ ] UI calls to back-end APIs are not too chatty or chunky
- [ ] services are not directly referenced (only through dependency injection or service calls).  reference abstractions and not concrete types
- [ ] business volatilities are properly encapsulated (minimal coupling, high cohesion, and information hiding)
- [ ] new methods are contracts following detailed design
- [ ] new data contracts follow detailed design
- [ ] no behavior being passed between layers, data contracts are only data
- [ ] contracts are being mapped properly between layers

### General code review
- [ ] code format/styling/casing follows standards
- [ ] configuration file changes are correct
- [ ] no secure credentials are stored in the source code
- [ ] code is self-documenting
- [ ] user variable names
- [ ] comments
- [ ] one class, data structure, interface, or enum per file
- [ ] exceptions are handled properly
- [ ] logging has been added to new code
- [ ] new external libraries have the proper license
- [ ] new external libraries are encapsulated correctly
- [ ] existing frameworks are on the latest stable version where possible

### New projects
- [ ] name-spacing is correct
- [ ] new project belongs in this situation
- [ ] code belongs in a new project and not an existing project

### Database changes
- [ ] upgrade scripts account for all code changes
- [ ] data types for new fields are correct
- [ ] no logic was added to the database that belongs in the code
- [ ] no scalability concerns exist for new data
- [ ] indexes are properly defined
- [ ] foreign keys are properly defined

### UI changes
- [ ] design comps were followed
- [ ] the client-side architecture was followed

