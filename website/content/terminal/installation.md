# Docker Installation

To install OpenBBTerminal using Docker, follow these steps:

1. Install Docker on your machine. Refer to the official Docker documentation for instructions specific to your operating system.

2. Clone the OpenBBTerminal repository from GitHub:

   ```console
   git clone https://github.com/OpenBB-finance/OpenBBTerminal.git
   ```

3. Navigate to the cloned repository:

   ```console
   cd OpenBBTerminal
   ```

4. Build the Docker image:

   ```console
   docker build -f build/docker/api.dockerfile -t openbb-platform:latest .
   ```

5. Run the Docker container:

   ```console
   docker run --rm -p 8000:8000 -v ~/.openbb_platform:/root/.openbb_platform openbb-platform:latest
   ```

   This command will mount the local `~/.openbb_platform` directory into the Docker container to use with the API keys and preferences. It will also expose the API on port `8000`.

6. Access OpenBBTerminal by opening a web browser and navigating to `http://localhost:8000`.

That's it! You have successfully installed and run OpenBBTerminal using Docker.
