FROM mcr.microsoft.com/dotnet/core/sdk:3.0.100-preview8

# Install fake
RUN dotnet tool install fake-cli -g

# Install Paket
RUN dotnet tool install paket -g

# add dotnet tools to path to pick up fake and paket installation
ENV PATH="/root/.dotnet/tools:${PATH}"

# Copy endpoint specific user settings into container to specify
# .NET Core should be used as the runtime.
COPY settings.vscode.json /root/.vscode-remote/data/Machine/settings.json
