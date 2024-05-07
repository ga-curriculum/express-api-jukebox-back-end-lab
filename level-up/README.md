# ![Express API - Jukebox Lab - Level Up](./assets/hero.png)

## Level Up

As you become more comfortable with the basics of your Jukebox API, you can enhance the application's functionality and user experience by adding more features. Here are some "Level Up" features that will not only make your application more robust but also more engaging:

### Expanded track model

Expand the `Track` model to include additional properties that add to the track information and user experience:

- **Cover Art URL**: Include a URL to an image that represents the cover art of the track.
- **Sound Clip URL**: Provide a link to a short sound clip of the track, possibly via an external music API.

### Updated track model entity

| Field       | Type   | Required | Description                                   |
| ----------- | ------ | -------- | --------------------------------------------- |
| title       | String | Yes      | The title of the track.                       |
| artist      | String | Yes      | The artist of the track.                      |
| time        | String | No       | The runtime of the track, optional.           |
| coverArtUrl | String | No       | URL to the track's cover art image, optional. |
| soundClipUrl| String | No       | URL to a sound clip of the track, optional.   |

### Integration with external music API

- Integrate with an external music API to fetch sound clips for each track. This could involve:
  - Researching and choosing an appropriate music API that provides sound clip functionality.
  - Implementing API calls from your backend to retrieve sound clips when adding or updating tracks.

Happy Coding!
