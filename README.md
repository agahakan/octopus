# octopus
handy knowledge of a clean and efficient way of configuring machines

The poll application starts with a Python Flask web client that gathers the votes, and then
pushes them into a Redis queue. Afterwards, the Java worker consumes the votes stored in the Redis queue,
and pushes them into a PostgreSQL database. Finally, the Node.js web client fetches the votes from the
PostgreSQL database and displays the results.

With Ansible, we deploy  the application onto 5 different machines, without using containers.
