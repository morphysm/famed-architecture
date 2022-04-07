# famed-architecture
Architecture, Specification and Documentation of famed 

## Famed Data Flow
![Famed Flow](https://user-images.githubusercontent.com/11260050/162227373-3010ac5d-3f13-4d38-8e86-471d800404fd.png)

### Walls of Fame
The Walls of Fame frontend requests the list of contributors from the Famed BFF (Backend for Frontend), when a user vistis the Walls of Fame website. The Fame BFF then calls the Github API and requests all Github Issues of the repo. The Github Issues are filtered by qualifying properties, closed and labeled “Fame”. For each qualifying issue the Github Issue Events are requested from the Github API. Based on the events and the issue information, a list of contributors is generated and populated with information about performance and rewards. The list is then returned to the Fame Board frontend and displayed to the user.

### Famed GitHub App
If the GitHub App is installed in a Repo with Issue/Pull Request and Webhook permissions, GitHub sends an Event to the Famed BFF using the registered Webhook each time a Issue is changes. The Famed BFF filters the events for changes that are relevant. If a relevant change occures a new Comment is posted or a current comment is updated via the GitHub API.
