# How to use this package? 👀
+ Install the package from `pip`
```powershell
pip install scrape-up
```

+ Scrape the required information, for example one want to extract number of followers of a user.
```python
# Import the required module
from scrape_up import github

# Instantiate an object with username provided.
user = github.User(username="nikhil25803")

# Cal the followers function
print(user.followers())

# Output - '59'
```

---

# The platforms and methods we cover 💫

## GitHub
```python
from scrape_up import github
```

### Scrape User details

First create an object of class `User`
```python
user = github.Users(username="nikhil25803")
```

| Methods |  Details |
|---|---|
|  `.followers()` | Returns the number of followers of a user. |
|  `.get_avatar()` | Returns the avatar url of a user. |
|  `.get_bio()`  | Returns the bio of a user. |
|  `.get_repo()` | Returns the list of pinned repositories for a user. |
|  `.repo_count()` | Returns the number of Repositories of a user. |
|  `.star_count()` | Returns the number of stars of a user. |
|  `.get_yearly_contributions()` |Returns the number of contributions made in 365 days frame. |
|  `.get_repositories()` | Returns the list of repositories of a user. |
|  `.get_starred_repos()` | Return the list of starred repositories of a user. | 
|  `.pul_requests()` |Return the number of pull requests opened in a repository. |

|  `following()`  | Returns the number of following of a user. |

-----

### Scrape Repository details

First create an object of class `Repository`
```python
repository = github.Repository(username="nikhil25803", repository_name="scrape-up")
```

| Methods | Details                                                     |
|---|-------------------------------------------------------------|
|  `.fork_count()` | Returns the number of forks of a repository.                |
|  `.topics()` | Returns the topics of a repository.                         |
|  `.pull_requests()` | Returns the number of pull requests opened in a repository. |
|  `.tags()` | Returns the last ten tags of a repository.                  |
|  `.releases()` | Returns the last ten releases of a repository.                  |
|  `.issues_count()` | Returns number of issues in a respository |
|  `.readme` | Saves the readme.md file of given user to current working directory. To view the readme.md with live server, change ".md" to ".html" in "readme.md". |
|  `.get_pull_requests_ids()` | Returns all id's of opened pull requests in a repository. |
|  `.get_issues()` | Returns list of all open issues in a repository. |

------------

### Scrape an issue details

First create an object of class `Repository`
```python
repository = github.Issue(username="nikhil25803", repository_name="scrape-up", issue_number=59)
```


| Methods        | Details                                                        |
|----------------|----------------------------------------------------------------|
| `.assignees()` | Returns the assignees of an issue.                             |
|  `.labels()`     | Returns the labels of an issue.                    |
| `.opened_by()` | Returns the name of the user, who opened the issue. |
|  `.title()`     | Returns the title of an issue.                    |

------------

### Scrape a pull request details

First create an object of class `Repository`
```python
repository = github.PullRequest(username="nikhil25803", repository_name="scrape-up", pull_request_number=30)
```


| Methods      | Details                                               |
|--------------|-------------------------------------------------------|
| `.commits()` | Returns the number of commits made in a pull request. |
| `.title()`   | Returns the title of a pull request.                  |
