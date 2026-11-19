# Program Showcase: Evergreen Quote
Five slides OR one page. Target: 5 minutes spoken, then 3 minutes of questions. Your audience on Friday afternoon includes your managers; assume they have not seen the program from the inside.

## Slide 1: Delivery goal & did we hit it?
- Goal (one sentence): A functional Evergreen Quote application is launched after a green CI build and merged PR, including connected marketing page, React app, API with database, and scaling provided by containerization.
- Hit? x Yes  ☐ Partially  ☐ No
- The delivery goal was hit, since all parts of the planned work were completed and able to be demoed locally.

## Slide 2: What shipped
- A screenshot of the wired app: the quote page showing quotes that came from the database.
- Link to the merged PR: https://github.com/asc1-student15/evergreen-quote-launch/pull/12
- Link to the green two-job CI run: https://github.com/asc1-student15/evergreen-quote-launch/actions/runs/44567187452

## Slide 3: Two key decisions
- **Decision 1:**
We decided to keep updated premium calculations synced between Cient and API allowing both customers and back end users to access the same quoting strategy and functionality. Keeping everything up to date is a little more effort, but it will be worth the extra time and network calls.
- **Decision 2:**
We decided to use the Copilot-proposed quotes in seeding since they were created in the right schema, with accurate data and correctly calculated premiums. The schema validation also passed when running 'npm run seed', which gave us further confidence in the result.


## Slide 4: Risks & injects
- Top risk we tracked: There's a mismatch in quotes displayed when the page is loaded and checked against the database
- Inject #1 (Tue):
In response to the requested changes today, our development team has decided to allow the updates to prioritize Life Coverage on the hero and dropdown boxes, as the changes just require reordering. Renter's Coverage was added as a fast-follow from last week's work, so that will be delivered and had already been accounted for.
For the demo on Friday, we will move forward with our original plan locally. There is no need to engage the cloud. We plan to walk through the kind cluster running on the VM, the kubectl service, the evergreen-quote-api on port 3000, and the interactive wired client in the browser.
- Inject #2 (Wed): 
In response to the failures reported today, I will have the platform development team revisit their 'cleanup' effort where it seems they have inadvertently renamed the Mongo DB application and prevented our pods from being able to find it. This seems to have caused the Crash Loop the manager is experiencing in the demo environment. To be clear, the database itself has not had changes and is still functional as is; the connection to it is just broken at the moment. This will be addressed by end of day today and I will get a report back from my team in the morning. At that time, I will advise if the fix is in place for your manager to retry their pre-launch dry run. Please let me know if there is anything else found suspicious within our current demo set up and I will have it investigated immediately so that the demo can proceed as planned.

## Slide 5: What three phases built
- An Evergreen Insurance landing page which redirects the user to a static quoting page rendered in HTML, a live React application working in the background to provide instant quotes, an API backed with a Mongo database for storage and retrieval, and all containerized into a well orchestrated product.
- Takeaway: I will take back to my work the ability to better type-check our code (most of our applications use typescript and Node). This will help us catch errors earlier at the local level instead of once code is commited for review.
- One thing I'd do differently next round: I would prioritize more time for this course and the capstone work specifically.

## Q&A prep: likely questions
Why didn't I deploy up to EKS? I ran out of time Thursday and it was not required.
