# Bug REPRODUCTION

1. From VsCode Command Pallete RUN `Remote-Containers: Rebuild without Cache and Reopen in container` 
2. Notice upon finishing that the `"postCreateCommand": "sudo chown $(whoami) node_modules",` in `devcontainer.json` doesn't break
3. Notice upon finishing that the `"postStartCommand": "npm install",` in `devcontainer.json` doesn't break
4. From VsCode Command Pallete RUN `Remote-Containers: Reopen Folder Locally`
5. Uncomment either `"PATH"` variable under the `remoteEnv` property in the `devcontainer.json`
6. From VsCode Command Pallete RUN `Remote-Containers: Rebuild without Cache and Reopen in container` 
7. Notice upon finishing that the `"postCreateCommand": "sudo chown $(whoami) node_modules",` in `devcontainer.json` breaks
8. Notice upon finishing that the `"postStartCommand": "npm install",` in `devcontainer.json` breaks
