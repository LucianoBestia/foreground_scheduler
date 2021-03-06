# foreground_scheduler  

[comment]: # (lmake_readme cargo.toml data start)
version: 2020.507.1304  date: 2020-05-07 authors: Luciano Bestia  
**runs a command at interval in foreground**

[comment]: # (lmake_readme cargo.toml data end)

## screen instead of background

In Linux I love to use the screen command. In a screen session I can run a program
and detach with `ctrl+a, d`.
The program will run indefinitely. With `screen -r name` I can attach the session again and see
what is going on. And then detach again.  
Watching the stdout of the program "in foreground" is easier then reading logs. This is from the viewpoint of a developer. I want to see my program how it works after every modification.  
This is great for beta web servers. They need to run indefinitely.  
For other tasks like fetching data every hour I need a scheduler. The scheduler will run indefinitely inside a screen. The fetch program will run for a few seconds every hour.  

## Run

Run it with this arguments minute, command, args:  

`foreground_scheduler 4 cargo "crev repo fetch trusted"`  
This will run every hour at xx:04 minutes.  

## Development

Documentation:  
<https://lucianobestia.github.io/foreground_scheduler>  
List of prepared make tasks for development: build, run, doc, publish,...  
`clear; cargo make release`  
`clear; cargo make run_rel1`  

## cargo crev reviews and advisory

It is recommended to always use [cargo-crev](https://github.com/crev-dev/cargo-crev)  
to verify the trustworthiness of each of your dependencies.  
Please, spread this info.  
On the web use this url to read crate reviews. Example:  
<https://web.crev.dev/rust-reviews/crate/num-traits/>  

