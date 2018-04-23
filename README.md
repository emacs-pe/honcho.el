# honcho - Run and manage long-running services

*Author:* Mario Rodas <marsam@users.noreply.github.com><br>
*Version:* 0.1<br>

Manage external services from within Emacs.

### Defining services

A minimal example to define a service with `honcho-define-service`

        (honcho-define-service python-server
          :command ("python" "-m" "http.server"))

To list the services, use <kbd>M-x honcho</kbd>.  There is also <kbd>M-x honcho-procfile</kbd> to
load services from a Procfile.

        (honcho-define-service node-server
          :command ("node" "server.js")
          :cwd     "/path/to/project/"
          :env     (("NODE_ENV"  . "development")
                    ("REDIS_URL" . "redis://localhost:6379/0")))

### Troubleshooting

+ **The service buffer contains ANSI control sequences**

  `honcho` uses `compilation-mode` underneath, it's recommended to setup
  [xterm-color][] for `compilation-mode`.

### Related projects

+ [prodigy.el][]: Manage external services from within Emacs

[prodigy.el]: https://github.com/rejeep/prodigy.el
[xterm-color]: https://github.com/atomontage/xterm-color


---
Converted from `honcho.el` by [*el2markdown*](https://github.com/Lindydancer/el2markdown).
