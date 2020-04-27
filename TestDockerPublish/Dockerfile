#See https://aka.ms/containerfastmode to understand how Visual Studio uses this Dockerfile to build your images for faster debugging.

FROM microsoft/dotnet:latest
WORKDIR /app
COPY /. /app
RUN dotnet restore
RUN dotnet publish -o /out -c Release
EXPOSE 443
ENTRYPOINT ["dotnet", "TestDockerPublish.dll"]