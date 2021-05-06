# Prototype-Mock-API

Mock API using JSON Server

JSON Server Repo: https://github.com/typicode/json-server
See Egghead video: https://egghead.io/lessons/javascript-creating-demo-apis-with-json-server

use `npx json-server db.json`

## Trouble Shooting

Does not seem to like running in create-react-app as it has it's own public folder. This will return a 404 on the homepage.
See: https://github.com/typicode/json-server/issues/1100#issue-578574593

To run with create-react-app create a JSON-Server config file `json-server.json`.

Add the following:

```json
{
  "port": 3001,
  "static": "'./node_modules/json-server/public'"
}
```

Now run:
`npx json-server db.json`
