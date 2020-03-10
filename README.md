## Docker with multiple web app

A little demo setup for multiple web app working with docker.

The first container named next uses nextjs and its SSR.

The second container named react uses create-react-app and its SPA.

The lasted container named nginx-proxy listens on port 3000 for next and 5000 for 5000 as a transfer station.

### Docker Compose

install Docker and Docker-compose and run:

```bash
docker-compose up
```

Then you will see nextjs demo and reactjs demo page at [http://localhost:3000](http://localhost:3000) and [http://localhost:5000](http://localhost:5000)

### Explanation

Maybe it's no need to combine all projects and we may restart all project even if a little change. We can use nginx globally to work with each project. Only reason I do this is that i just want to start by running `git clone url && docker-compose up` . Hard to say,I feel confused when installing and setting nginx in Linux at the beginning.
