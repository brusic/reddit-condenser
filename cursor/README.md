# Reddit User Posts & Comments Viewer

A web application that retrieves and displays Reddit posts and comments from a specific user in a subreddit within the past week.

## Features

- **User-friendly Interface**: Modern, Reddit-inspired dark theme UI
- **Post Retrieval**: Fetches all posts from a specific user in a chosen subreddit
- **Comment Hierarchy**: Displays comments in their proper nested structure
- **Time Filtering**: Only shows posts from the past week
- **Statistics**: Shows total posts, comments, and scores
- **Responsive Design**: Works on desktop and mobile devices

## How to Use

### Method 1: Interactive Form
1. **Open the Application**: Open `index.html` in your web browser
2. **Enter Details**:
   - **Reddit Username**: Enter the Reddit username (without u/) - Optional
   - **Subreddit**: Enter the subreddit name (without r/) - Required
   - **Title Search**: Enter keywords to search in post titles - Optional
   - **Post Limit**: Number of posts to fetch (1-100, default: 25)
   - **Time Filter**: Select time range for posts (default: All Time)
3. **Fetch Data**: Click "Fetch Posts & Comments" or press Enter
4. **View Results**: The application will display all posts and their comments

### Method 2: URL Parameters
You can also set initial values using URL parameters, which works even when opening the file locally:

```
file:///path/to/index.html?subreddit=programming&username=AutoModerator&limit=50
```

#### Supported URL Parameters:
- `subreddit` - The subreddit to search (required for auto-fetch)
- `username` - Reddit username to filter by
- `title` - Keywords to search in post titles
- `limit` - Number of posts to fetch (1-100)
- `time` - Time filter (hour, day, week, month, year, all)

#### Example URLs:
```
# Basic subreddit search
file:///path/to/index.html?subreddit=AskReddit

# User-specific posts
file:///path/to/index.html?subreddit=announcements&username=spez

# Title search with custom limit
file:///path/to/index.html?subreddit=programming&title=javascript&limit=10

# Combined search
file:///path/to/index.html?subreddit=AskReddit&username=AutoModerator&title=rules&limit=5

# Time-filtered search
file:///path/to/index.html?subreddit=programming&time=day&limit=10
```

## Example Usage

- **Username**: `spez`
- **Subreddit**: `announcements`
- **Title Search**: `update`
- **Limit**: `50`
- **Time Filter**: `week`

This will fetch up to 50 posts by u/spez in r/announcements containing "update" in the title from the past week.

## Technical Details

### API Usage
- Uses Reddit's public JSON API
- No authentication required for public data
- Respects Reddit's rate limiting

### Data Processing
- Filters posts by subreddit and time (past week)
- Processes comment hierarchy recursively
- Skips deleted/removed comments
- Maintains chronological order

### Features
- **Error Handling**: Graceful error handling for network issues
- **Loading States**: Visual feedback during data fetching
- **Input Validation**: Ensures required fields are filled
- **Responsive Layout**: Adapts to different screen sizes

## Browser Compatibility

- Modern browsers with ES6+ support
- Requires JavaScript enabled
- No external dependencies

## Limitations

- Limited to public Reddit data
- Subject to Reddit's API rate limits
- Only fetches posts from the past week
- Comments are limited to what's publicly available

## File Structure

```
├── index.html          # Main application file
└── README.md          # This documentation
```

## Troubleshooting

- **No posts found**: Check that the username and subreddit are correct
- **Network errors**: Ensure you have an internet connection
- **Empty results**: The user may not have posted in that subreddit recently

## Privacy

This application only accesses publicly available Reddit data and does not store any personal information.
