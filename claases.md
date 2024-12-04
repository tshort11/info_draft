# **Detailed Documentation of Classes, Functions, and Imported Packages**

## **Custom Classes**

### **1. Class: `User`**
- **Purpose**:  
  Represents a user within the music app with attributes for username, email, password, and lists for favorite albums, songs, and artists.  
- **Attributes**:  
  - `user_id` (int): A unique ID for the user.  
  - `username` (str): The user's username.  
  - `email` (str): The user's email address.  
  - `password` (str): Encrypted password for login.  
  - `favorite_albums` (list): Stores the user's favorite albums.  
  - `favorite_songs` (list): Stores the user's favorite songs.  
  - `favorite_artists` (list): Stores the user's favorite artists.  
- **Methods**:  
  - `add_favorite_album(album)`: Adds an album to the user's favorite albums.  
  - `add_favorite_song(song)`: Adds a song to the user's favorite songs.  
  - `add_favorite_artist(artist)`: Adds an artist to the user's favorite artists.  

---

### **2. Class: `Album`**
- **Purpose**:  
  Represents a music album with attributes for title, artist, release date, and rating.  
- **Attributes**:  
  - `album_id` (int): Unique identifier for the album.  
  - `title` (str): The album's title.  
  - `artist` (str): Name of the artist(s).  
  - `release_date` (str): The album's release date.  
  - `rating` (float): User's rating for the album.  

---

### **3. Class: `Song`**
- **Purpose**:  
  Represents a song with attributes for title, artist, album, and duration.  
- **Attributes**:  
  - `song_id` (int): Unique identifier for the song.  
  - `title` (str): Song title.  
  - `artist` (str): Name of the artist.  
  - `album` (str): The album the song belongs to.  
  - `duration_ms` (int): The song's duration in milliseconds.  

---

### **4. Class: `Artist`**
- **Purpose**:  
  Represents a music artist with attributes for name and genre.  
- **Attributes**:  
  - `artist_id` (int): Unique identifier for the artist.  
  - `name` (str): Artist's name.  
  - `genre` (str): Genre of the artist's music.  

---

## **Custom Functions**

### **1. Function: `add_favorite_album_with_rating(user, spotify)`**
- **Purpose**:  
  Allows the user to add albums to their favorites with a rating.  
- **Parameters**:  
  - `user` (User): The logged-in user.  
  - `spotify` (SpotifyAPI): An instance of the Spotify API class for retrieving album details.  
- **Returned Result**:  
  None. Updates the `User` object with the album.  

---

### **2. Function: `discover_music(user, spotify)`**
- **Purpose**:  
  Displays new releases from Spotify's API.  
- **Parameters**:  
  - `user` (User): The logged-in user.  
  - `spotify` (SpotifyAPI): An instance of the Spotify API class to fetch new releases.  
- **Returned Result**:  
  None. Outputs a list of new releases to the terminal.  

---

### **3. Function: `view_user_info(user)`**
- **Purpose**:  
  Displays all user profile information, including favorite albums, songs, and artists.  
- **Parameters**:  
  - `user` (User): The logged-in user whose information is displayed.  
- **Returned Result**:  
  None. Outputs data to the terminal using `PrettyTable`.  

---

## **Imported Code or Packages**

### **1. `json`**
- **Purpose**:  
  Handles saving and loading user data to/from a JSON file.  
- **Used For**:  
  - Serializing user data (`save_users`).  
  - Deserializing data (`load_users`).  

---

### **2. `rich.console.Console`**
- **Purpose**:  
  Provides colorful terminal output to enhance the user interface.  
- **Used For**:  
  - Styling text in prompts and outputs during application interactions.  

---

### **3. `prettytable`**
- **Purpose**:  
  Creates formatted tables to display user information like albums, songs, and artists.  
- **Used For**:  
  - Making profile data more readable (`view_user_info`).  

---

### **4. `SpotifyAPI` (Custom Class)**
- **Purpose**:  
  Manages communication with the Spotify API to fetch music data (albums, songs, artists).  
- **Used For**:  
  - Retrieving album details in `add_favorite_album_with_rating`.  
  - Fetching new releases in `discover_music`.  

---

### **5. `os`**
- **Purpose**:  
  Checks for the existence of the `users.json` file.  
- **Used For**:  
  - Ensuring user data persistence across sessions.  

---

## **Usage Summary**
- **Core Functionality**:  
  - Classes and methods manage user accounts, preferences, and interactions with the Spotify API.  
- **User Experience Enhancements**:  
  - Libraries like `rich` and `prettytable` improve terminal interaction and readability.  
- **Data Persistence**:  
  - Libraries such as `json` and `os` ensure seamless saving and loading of user data.  
