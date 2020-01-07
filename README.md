# <img src="https://github.com/pip-services/pip-services/blob/master/design/Logo.png" alt="Pip.Services Logo" style="max-width:30%"> <br/> Library of Reusable Microservices

Unique features of [Pip.Services toolkit](http://github.com/pip-services/pip-services)
allowed to create a library of reusable microservices that are due to the flexible componentized
design can be configured to run on any platform, use variety of persistent and communication
technologues and integrate with large number of infrastructure services. 

<div style="border: 1px solid #ccc">
  <img src="design/Overview.png" alt="Pip.Services Overview" style="display:block;">
</div>

The library contains constantly growing number of microservices, donated and supported by community contributors.
They divided into several groups.

### Infrastructure microservices
- [pip-services-logging](https://github.com/pip-services-infrastructure/pip-services-logging-node) - Distributed logging microservice. 
It collects logs from other microservices and stores them in a single location for further analysis.
- [pip-services-counters](https://github.com/pip-services-infrastructure/pip-services-counters-node) - 
Performance monitoring microservice. It collects performance metrics from other microservices and generates 
performance statistics.
It is a lightweight alternative to production services like Consul or Etcd that can be used during development and testing.
- [pip-services-eventlog](https://github.com/pip-services-infrastructure/pip-services-eventlog-node) - System event logging microservice. 
It logs key system events like installing a new server, upgrading to a newer version, shutting down system for maintenance
and so on
- [pip-services-settings](https://github.com/pip-services-infrastructure/pip-services-settings-node) - Settings microservice. 
It keeps system-wide configuration settings split by sections.
- [pip-services-statistics](https://github.com/pip-services-infrastructure/pip-services-statistics-node) - Statistics microservice. 
It aggregates business statistics within Hour, Day, Month, Year and Total intervals.
- [pip-services-metrics](https://github.com/pip-services-infrastructure/pip-services-metrics-node) - Metrics microservice. 
Yet another analytical service that collect business metrics/statistics within Hour, Day, Month, Year and Total intervals with ability to break them down into multiple dimensions.
- [pip-services-blobs](https://github.com/pip-services-infrastructure/pip-services-blobs-node) - Blob storage microservice. 
It is the key microservice that enables upload and download of binary blobs. It also tracks references from other system entities and destroys files when the last reference is released.
- [pip-services-facets](https://github.com/pip-services-infrastructure/pip-services-facets-node) - Faceted search microservice. 
It records and allows to search by aggregated (faceted) criteria, like groups, types or categories.
- [pip-services-changescopes](https://github.com/pip-services-infrastructure/pip-services-changescopes-node) - Change scopes microservice.
It trackes changes in specific scope down to individual elements. That helps to use simple pulls to detect changes in one call without use of asynchronous update messages.
- [pip-services-email](https://github.com/pip-services-infrastructure/pip-services-email-node) - Email delivery microservice. It sends email messages and supports message templates.
- [pip-services-sms](https://github.com/pip-services-infrastructure/pip-services-sms-node) - SMS delivery microservice. It sends sms messages and supports message templates.
- [pip-services-clusters](https://github.com/pip-services-infrastructure/pip-services-clusters-node) - Clusters microservice. 
It keeps records of all computational and data clusters of a system and defines where tenant data and logic are located. This microservice is handy to implement partitioning of data or/and processes to achieve horizontal scalability.
- [pip-services-jobs](https://github.com/pip-services-infrastructure/pip-services-jobs-node) - Jobs queue microservice. 
It allows to schedule and distribute computational jobs among worker services.

### User management microservices
- [pip-services-accounts](https://github.com/pip-services-users/pip-services-accounts-node) - Users account management microservice. 
It allows to register system users and set their key preferences.
- [pip-services-passwords](https://github.com/pip-services-users/pip-services-passwords-node) - Password authentication microservice. 
It allows to set and manage user password, performs basic login/password based authentication and supports password 
recovery via email.
- [pip-services-roles](https://github.com/pip-services-users/pip-services-roles-node) - User role-based authorization microservice. 
It allows to grant roles to a user and performs basic ‘is user in role’ authorization.
- [pip-services-emailsettings](https://github.com/pip-services-users/pip-services-emailsettings-node) - Email settings microservice. 
It manages user primary emails and handles email verification.
- [pip-services-smssettings](https://github.com/pip-services-users/pip-services-smssettings-node) - SMS settings microservice. 
It manages user phone numbers and handles phone verification.
- [pip-services-msgdistribution](https://github.com/pip-services-users/pip-services-msgdistribution-node) - Message distribution microservice. 
It distributes messages to one or many recipients via selected delivery method: email or sms.
- [pip-services-sessions](https://github.com/pip-services-users/pip-services-sessions-node) - User session management microservice. 
It tracks sessions opened by users from multiple hosts and applications. It can be very useful for session tracking 
in client facades (API gateways).
- [pip-services-activities](https://github.com/pip-services-users/pip-services-activities-node) - User/party activity logging microservice. 
It logs activities performed by user (or party) like registering and logging into the system, changing configuration settings, 
creating/removing/updating system entities and so on.
- [pip-services-organizations](https://github.com/pip-services-users/pip-services-organizations-node) - Organizations management microservice. 
It keeps track of organizations registered in a system.
- [pip-services-orgroles](https://github.com/pip-services-users/pip-services-orgroles-node) - Organizational roles microservice. 
It manages user roles in relation to organization access rights.
- [pip-services-invitations](https://github.com/pip-services-users/pip-services-invitations-node) - User invitation microservice. 
It sends out and manages invitations to new users and allows to grant them access to organizations where they were invited to.

### Product support microservices

- [pip-services-announcements](https://github.com/pip-services-support/pip-services-announcements-node) - System announcements microservice. 
It allows system administrators or product support personnel to create announcements and show them to product users to keep 
them informed about important information and events.
- [pip-services-feedbacks](https://github.com/pip-services-support/pip-services-feedbacks-node) - Users feedback microservice. 
It allows to collect feedback from product users about their issues, ideas, copyright infringement or other requests.

### Content management microservices

- [pip-services-attachments](https://github.com/pip-services-content/pip-services-attachments-node) - Blob attachments microservice. 
It tracks references to blobs from other system entities and destroys files when the last reference is released.
- [pip-services-tags](https://github.com/pip-services-content/pip-services-tags-node) - User/party search tags microservice. 
It records tags used by user (or party) when they create their content. Later these tags can be used to suggest tags 
for search within applications.
- [pip-services-quotes](https://github.com/pip-services-content/pip-services-quotes-node) - Inspirational quotes microservice. 
It is a basic sample microservice that shows to users inspiring quotes.
- [pip-services-tips](https://github.com/pip-services-content/pip-services-tips-node) - User tips microservice. 
It shows prerecorded useful tips and suggestions to application users.
- [pip-services-guides](https://github.com/pip-services-content/pip-services-guides-node) - Application guides microservice. 
It shows guides (introduction, walk-through, new release) to application users.
- [pip-services-imagesets](https://github.com/pip-services-content/pip-services-imagesets-node) - Image library microservice. 
It contains a collection of images that users can search and use to visualize their content.
- [pip-services-files](https://github.com/pip-services-content/pip-services-files-node) - Files microservice. 
It keeps collections (groups) of files. File content can be stored either in blobs or in external source and referenced via uri.
- [pip-services-msgtemplates](https://github.com/pip-services-content/pip-services-msgtemplates-node) - Message templates microservice. 
It allows content managers to compose message templates in multiple languages and later use to send out emails or sms to system users or internet community.
- [pip-services-dashboards](https://github.com/pip-services-content/pip-services-dashboards-node) - Dashboards microservice. 
It stores configurations of user dashboards.

### eCommerce microservices

- [pip-services-creditcards](https://github.com/pip-services-ecommerce/pip-services-creditcards-node) - Credit cards microservice. 
It stores customer credit cards in trusted places like PayPal.

## Quick Links

- [Pip.Services microservices toolkit](http://github.com/pip-services/pip-services)
- [Pip.Services discussion forum](https://groups.google.com/forum/#!forum/pip-services)
- [Pip.Services team blog](https://pip-services.blogspot.com/)

## Acknowledgements

This project would not be possible without effort contributed by particular individuals.

- **Sergey Seroukhov** - the project founder, microservice architecture and runtime implementation
- **Mark Zontak** - Node.js and .NET implementations, AWS integration
- **Volodymyr Tkachenko** - .NET implementation, Service Fabric and Docker deployments
- **Alex Mazur** - .NET implementations, Azure integration
- **Alex Masliev** - Website and graphics

We also would like to recognize help received from the following companies.

- **Digital Living Software Corp.**
- [**Modular Mining Systems Inc.**](http://www.mmsi.com)
- [**BootBarn**](http://www.bootbarn.com)
- [**EPAM**](http://www.epam.com)
- [**Kyrio**](http://www.kyrio.com)
- [**MST Global**](http://www.mstglobal.com)
- [**IQuipsys Inc.**](http://www.iquipsys.com)
