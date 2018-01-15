# Create Dockerized Rails App
```docker-compose run --rm web rails new . -T -f```

Description:
```docker-compose run ``` Run (a command)
```--rm ``` removing the container after run
```web ``` into the 'web' service (declared into docker-compose.yml [line 3])
```rails new . ``` the command 'rails new' to create a new rails app into the current directory ('.')
```-T ``` [--skip-test] skipping test files
```-f ``` [--force] overwritting files that already exist (Gemfile, Gemfile.lock)

If you are running Docker on Linux the container runs as the root user by default. If you omit the --user flag you must change the ownership of the files (```sudo chown -R $USER:$USER .```)

## For more infomation
[docker-compose run command (Docker Docs)](https://docs.docker.com/compose/reference/run/)
[The Rails Command Line: rails new (Rails Guides)](http://guides.rubyonrails.org/command_line.html#rails-new)
[Quickstart: Compose and Rails (Docker Docs)](https://docs.docker.com/compose/rails/)