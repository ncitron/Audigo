# Audigo
A Go Wrapper for Music APIs - Last.fm, Spotify

Under construction, check back later!

## Docs

### Spotify
**spotify.SpotifyClient{ClientId string, ApiSecret string, AccessToken string)**
- ClientId: Spotify API Client Id
- ApiSecret: Spotify API Secret
- AccessToken: Spotify API Access Token if you have a valid one, otherwise pass empty string

*SpotifyClient.Authenticate() error*
- Uses SpotifyClient's ClientId and ApiSecret to generate a new API Access Token.
- IMPORTANT:This Must Be Run Before Any Other SpotifyClient method if you did not pass a valid AccessToken to the constructor

#### Albums

*SpotifyClient.GetAlbum(id string) (album SpotifyAlbum, e error)*
- id: Spotify Album Id

*SpotifyClient.GetAlbums(ids []string) (album SpotifyAlbums, e error)*
- ids: Slice of Spotify Album Ids

#### Artists

*SpotifyClient.GetArtistAlbums(id string) (albums ArtistAlbums, e error)*
- id: Spotify Artist Id
