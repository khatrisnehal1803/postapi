https://github.com/khatrisnehal1803/postapi/issues/1#issue-3218894038 



📄 React Pagination App – Description
This React app displays posts from a public API (JSONPlaceholder) with pagination.

🔗 API Used
URL:

arduino
Copy
Edit
https://jsonplaceholder.typicode.com/posts
Total posts available: 100

This app fetches posts 10 at a time (one page).

⚙️ Key Features
✅ Data Fetching

Uses fetch API to load posts from the server.

Automatically sends:

ini
Copy
Edit
_page={page}&_limit=10
in the URL to control pagination.

✅ State Management

State	Purpose
posts	Holds posts fetched from the API.
loading	Controls the loading spinner/message.
error	Stores any error messages from the API.
page	Keeps track of the current page number.

✅ Pagination Controls

Total Pages: 10 (hard-coded)

Previous Button:

➡ Goes to the previous page.

🔒 Disabled on page 1.

Next Button:

➡ Goes to the next page.

🔒 Disabled on page 10.

🖥️ User Interface
Displays:

A title → “Posts”

A loading message → “Loading…” while data is being fetched.

An error message if something goes wrong.

A list of posts:

Each post shows:

The serial number (e.g. 1., 2., 3. …)

The title in bold.

The body text below the title.

Pagination section:

Previous and Next buttons.

Current page number (e.g. “Page 4”).

🛠️ Technologies Used
React (Function Component)

Hooks:

useState → Manage local state

useEffect → Fetch data when page changes

Fetch API for HTTP requests

Simple CSS styling

⚡ How It Works
The app starts on Page 1.

When the app loads or the page changes:

It sends a request to the API for that page’s posts.

While waiting for data:

Shows Loading…

When data arrives:

Displays the list of posts.

If there’s an error:

Displays an error message.

Users click Next or Previous to see other posts.

📝 Example Post Display
markdown
Copy
Edit
1. sunt aut facere repellat provident occaecati excepturi optio reprehenderit
   quia et suscipit
   suscipit recusandae consequuntur expedita et cum
🚫 Edge Handling
No “Previous” on Page 1

No “Next” on Page 10

Displays an error if the API fails

This app is perfect as a beginner-friendly example of:

React data fetching

Loading & error handling

Pagination logic

Clean UI updates
