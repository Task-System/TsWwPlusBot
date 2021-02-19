![TsWwLogo](TsWwLogo.PNG)

# [TsWwPlusBot](https://t.me/tswwplus_bot)
Repo related to Telegram bot Task System 2 ([@TsWwPLus_Bot](https://t.me/tswwplus_bot))

## 🌙 Task System 2
Task system 2 is a telegram bot that is Known as ranking bot for [Werewolf games 🐺 in telegram](https://t.me/werewolfbot)

it's primary task is to **rank players and groups based on games played** in werewolf bot

Beside that task system has a lot of features that can come handy in groups (_specially werewolf and game groups_) management, such as:

    - Welcome message
    - Tagger
    - Personal points
    - Get werewolf stats
    - Role manage during the ww game
    - etc.

## 🗂 Source
Task System 2 source code is now available here for everyone

It's a **.NET project** written in C# and recentlly ported from .NET framework to **.NET Core 3.1**

## ☎ Contact options
If you wanna help us fix a bug or somthing like that you can simply open an issue right here.

**If you need some help about bot in telegram:**

_[TsWw Notifications](https://t.me/tsww_channel)_

_[TsWw Support Group (@TsWw\_Support)](https://t.me/tsww_support)_


## 🛠 Build and Run
if you are intersted in running this source from your private server, here is some tips:

### 🧱 Requierments
    - Have .NET Core 3.1 or higher SDK installed on your server
    - SQL Server 2016 or higher

### 📚 Make database
you can use Migration tools of Ef Core to build database, Migration files are available in repo dir

Simply run `Update-Database` in **PM Console**

_Don't forget to replace you db Connection String in Context File (`Context/Entities.cs`)_
```cs
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
{
    if (!optionsBuilder.IsConfigured)
    {
        optionsBuilder.UseSqlServer("RIGHT HERE");
    }
}
```

### 🎭 Secrets
Restore and build project using dotnet command

TsWw uses secret manager to store Bot token and connection string

store your secrets like below in a normal terminal and in _NewTsWw.sln_ dir:

```powershell
dotnet user-secrets set "Production:Token" "BOT_TOKEN" --id "b29db55a-d376-4865-858f-b6a871f4ff9a"
```

And repeat it 3 more times for :

    "Production:ConnectionString"
    "Development:Token"
    "Development:ConnectionString"

Ik that was not a complete tour, but it can help you run the bot if you have a little .NET experiance.

# Good Luck 😉














