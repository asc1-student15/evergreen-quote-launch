# Evergreen Quote: Vision Brief
Target length: 1 page (~300 words). Write for a Liberty Mutual VP who has 90 seconds.

## Product
**Name:** Evergreen Insurance Quote (the launch: full-stack delivery)
**Delivery week:** Final
**Delivery Lead:** Tina Matthys
**Engineering team (represented by):** https://github.com/asc1-student15/evergreen-quote-launch
**GitHub Project board:** https://github.com/users/asc1-student15/projects/4/views/1

## Who is the customer?
There are several 'customers' that will benefit from this launch. Externally served is the young adult seeking insurance for the first time, with no prior knowledge or patience for long processes or logging in. They want a fast quote on their phone with a premium they can trust and no strings attached. Internally we have a partner team that will use GraphQL to filter quotes using their specialized field values, along with an ops team who will have the service orchestrated and running with Kubernetes. In addition, we also invite our management teams to act as an audience to the completion of this full launch initiative.

## What pain does Evergreen Quote remove?
The customer-facing site removes the need to create an account, log in, and enter pages of information for a single quote.
The use of GraphQL allows each our partners to customize their database tables with fields that make sense for them, instead of being constrained to one specific schema.
The containerized orchestration allows our operations to scale over time, as needed, without loss of service during busy times.
Putting these pieces together gives the young insurance seeker once place to efficiently quote, save, retrieve and experiment with their insurance options.

## What does "good" look like at end of the week?
- The API should display the recent quotes list and the Save button should work to both add the result to the DB, plus append it to the visible list
- The Database should be functional, with saved quotes accessible to the application via API calls to GraphQL
- The look-and-feel of the website should adhere to the sponsor's preferences
- The CI workflow should test and build with a green result on each push, and merge to the 'main' branch
- The Kubernetes container should be set up to use the API image, packaged as `evergreen-quote-api:2.0`, with four pods (3 replicas + 1 DB) running on a `kind` cluster and able to save quotes

## What are we explicitly NOT doing this week?
- No authentication, no payments, no real rate engine.
- No AWS Account with actual spend - this work is done locally.

## How will we know if it worked?
- A quote saved in the browser survives a reload and shows the same premium
  the estimate promised.
- A Pull Request into `main` that includes changes to HTML, CSS, TypeScript, JavaScript, a Dockerfile, cluster
  manifests, and a CI config in one place.
- Both CI jobs are green on the merged `main`.
- The demo successfully shows the process from the website input, through the backend application and database, persisted on the cluster, and available to the customer upon next request.
