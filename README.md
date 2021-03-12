# Very Simple Web Socket Shell

This is an example of a very simple websocket based shell that you can run on Cloud Foundry.

This application uses [websocketd](https://github.com/joewalnes/websocketd/).

**THIS APPLICATION IS NOT SECURE IN ANY WAY AND SHOULD NEVER BE RUN IN A PRODUCTION SITUATION. IT IS FOR DEMONSTRATION PURPOSES ONLY**

## Instructions

1. Download the latest release of [websocketd](https://github.com/joewalnes/websocketd/releases). Pick the linux amd64 binary.
2. Extract the binary named `websocketd` from the archive. Place it in the root of the project.
3. [Optional] Adjust the route in the `manifest.yml` file.
4. Run `cf push`.
5. Access your application.

That will open up the [Dev Console](https://github.com/joewalnes/websocketd/wiki/console-count.png).

In the dev console address bar, type `wss://<route>/loop.sh` (the route should be auto-populated, but if not it should be the route you used to access your app).

The output should show open and onopen messages and then allow you to send commands to execute. The command's output will be returned, like a interactive shell.

Try sending `ps auxf` or some other fun commands.
