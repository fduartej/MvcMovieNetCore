git init
git config --global user.name ""
git config --global user.email ""


dotnet restore
dotnet aspnet-codegenerator controller -name MoviesController -m Movie -dc MvcMovieContext --relativeFolderPath Controllers --useDefaultLayout --referenceScriptLibraries
dotnet ef migrations add InitialCreate
dotnet ef database update


http://localhost:5000/Movies/