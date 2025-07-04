# action-repo"Test push event" 
# action-repo

This is a dummy GitHub repository used to test webhook events for an assessment task.

## Purpose

Whenever a GitHub event like **push**, **pull request**, or **merge** happens on this repo, it triggers a **webhook** that sends the event to a Flask server running in another repository (`webhook-repo`).

The Flask app stores the data in MongoDB, and the UI displays the events in real-time.

## How It Works

Push a new commit → Webhook sends event to Flask
Flask parses and stores event in MongoDB
UI (in `webhook-repo`) polls MongoDB every 15 seconds and shows updates

## Events Triggered

Push (tested)
Pull Request (optional)
Merge (optional)

