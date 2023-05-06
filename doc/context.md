# Context
## dumpするコード
```
name: Dump GitHub context
on:
  workflow_dispatch:

jobs:
  dump-context:
    runs-on: ubuntu-latest
    steps:
      - name: dump
        env:
          GITHUB_CONTEXT: ${{ toJson(github) }}
        run: |
          echo "$GITHUB_CONTEXT"
```

## 実行結果
```
{
  "token": "***",
  "job": "dump-context",
  "ref": "refs/heads/main",
  "sha": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "repository": "kdysk000/github_actions_samples",
  "repository_owner": "kdysk000",
  "repository_owner_id": "102411958",
  "repositoryUrl": "git://github.com/kdysk000/github_actions_samples.git",
  "run_id": "4900420084",
  "run_number": "3",
  "retention_days": "90",
  "run_attempt": "1",
  "artifact_cache_size_limit": "10",
  "repository_visibility": "public",
  "repository_id": "633883476",
  "actor_id": "102411958",
  "actor": "kdysk000",
  "triggering_actor": "kdysk000",
  "workflow": "Dump GitHub context",
  "head_ref": "",
  "base_ref": "",
  "event_name": "workflow_dispatch",
  "event": {
    "inputs": null,
    "ref": "refs/heads/main",
    "repository": {
      "allow_forking": true,
      "archive_url": "https://api.github.com/repos/kdysk000/github_actions_samples/{archive_format}{/ref}",
      "archived": false,
      "assignees_url": "https://api.github.com/repos/kdysk000/github_actions_samples/assignees{/user}",
      "blobs_url": "https://api.github.com/repos/kdysk000/github_actions_samples/git/blobs{/sha}",
      "branches_url": "https://api.github.com/repos/kdysk000/github_actions_samples/branches{/branch}",
      "clone_url": "https://github.com/kdysk000/github_actions_samples.git",
      "collaborators_url": "https://api.github.com/repos/kdysk000/github_actions_samples/collaborators{/collaborator}",
      "comments_url": "https://api.github.com/repos/kdysk000/github_actions_samples/comments{/number}",
      "commits_url": "https://api.github.com/repos/kdysk000/github_actions_samples/commits{/sha}",
      "compare_url": "https://api.github.com/repos/kdysk000/github_actions_samples/compare/{base}...{head}",
      "contents_url": "https://api.github.com/repos/kdysk000/github_actions_samples/contents/{+path}",
      "contributors_url": "https://api.github.com/repos/kdysk000/github_actions_samples/contributors",
      "created_at": "2023-04-28T13:57:34Z",
      "default_branch": "main",
      "deployments_url": "https://api.github.com/repos/kdysk000/github_actions_samples/deployments",
      "description": null,
      "disabled": false,
      "downloads_url": "https://api.github.com/repos/kdysk000/github_actions_samples/downloads",
      "events_url": "https://api.github.com/repos/kdysk000/github_actions_samples/events",
      "fork": false,
      "forks": 0,
      "forks_count": 0,
      "forks_url": "https://api.github.com/repos/kdysk000/github_actions_samples/forks",
      "full_name": "kdysk000/github_actions_samples",
      "git_commits_url": "https://api.github.com/repos/kdysk000/github_actions_samples/git/commits{/sha}",
      "git_refs_url": "https://api.github.com/repos/kdysk000/github_actions_samples/git/refs{/sha}",
      "git_tags_url": "https://api.github.com/repos/kdysk000/github_actions_samples/git/tags{/sha}",
      "git_url": "git://github.com/kdysk000/github_actions_samples.git",
      "has_discussions": false,
      "has_downloads": true,
      "has_issues": true,
      "has_pages": false,
      "has_projects": true,
      "has_wiki": true,
      "homepage": null,
      "hooks_url": "https://api.github.com/repos/kdysk000/github_actions_samples/hooks",
      "html_url": "https://github.com/kdysk000/github_actions_samples",
      "id": 633883476,
      "is_template": false,
      "issue_comment_url": "https://api.github.com/repos/kdysk000/github_actions_samples/issues/comments{/number}",
      "issue_events_url": "https://api.github.com/repos/kdysk000/github_actions_samples/issues/events{/number}",
      "issues_url": "https://api.github.com/repos/kdysk000/github_actions_samples/issues{/number}",
      "keys_url": "https://api.github.com/repos/kdysk000/github_actions_samples/keys{/key_id}",
      "labels_url": "https://api.github.com/repos/kdysk000/github_actions_samples/labels{/name}",
      "language": null,
      "languages_url": "https://api.github.com/repos/kdysk000/github_actions_samples/languages",
      "license": null,
      "merges_url": "https://api.github.com/repos/kdysk000/github_actions_samples/merges",
      "milestones_url": "https://api.github.com/repos/kdysk000/github_actions_samples/milestones{/number}",
      "mirror_url": null,
      "name": "github_actions_samples",
      "node_id": "R_kgDOJchLVA",
      "notifications_url": "https://api.github.com/repos/kdysk000/github_actions_samples/notifications{?since,all,participating}",
      "open_issues": 0,
      "open_issues_count": 0,
      "owner": {
        "avatar_url": "https://avatars.githubusercontent.com/u/102411958?v=4",
        "events_url": "https://api.github.com/users/kdysk000/events{/privacy}",
        "followers_url": "https://api.github.com/users/kdysk000/followers",
        "following_url": "https://api.github.com/users/kdysk000/following{/other_user}",
        "gists_url": "https://api.github.com/users/kdysk000/gists{/gist_id}",
        "gravatar_id": "",
        "html_url": "https://github.com/kdysk000",
        "id": 102411958,
        "login": "kdysk000",
        "node_id": "U_kgDOBhqutg",
        "organizations_url": "https://api.github.com/users/kdysk000/orgs",
        "received_events_url": "https://api.github.com/users/kdysk000/received_events",
        "repos_url": "https://api.github.com/users/kdysk000/repos",
        "site_admin": false,
        "starred_url": "https://api.github.com/users/kdysk000/starred{/owner}{/repo}",
        "subscriptions_url": "https://api.github.com/users/kdysk000/subscriptions",
        "type": "User",
        "url": "https://api.github.com/users/kdysk000"
      },
      "private": false,
      "pulls_url": "https://api.github.com/repos/kdysk000/github_actions_samples/pulls{/number}",
      "pushed_at": "2023-05-06T07:28:18Z",
      "releases_url": "https://api.github.com/repos/kdysk000/github_actions_samples/releases{/id}",
      "size": 198,
      "ssh_url": "git@github.com:kdysk000/github_actions_samples.git",
      "stargazers_count": 0,
      "stargazers_url": "https://api.github.com/repos/kdysk000/github_actions_samples/stargazers",
      "statuses_url": "https://api.github.com/repos/kdysk000/github_actions_samples/statuses/{sha}",
      "subscribers_url": "https://api.github.com/repos/kdysk000/github_actions_samples/subscribers",
      "subscription_url": "https://api.github.com/repos/kdysk000/github_actions_samples/subscription",
      "svn_url": "https://github.com/kdysk000/github_actions_samples",
      "tags_url": "https://api.github.com/repos/kdysk000/github_actions_samples/tags",
      "teams_url": "https://api.github.com/repos/kdysk000/github_actions_samples/teams",
      "topics": [],
      "trees_url": "https://api.github.com/repos/kdysk000/github_actions_samples/git/trees{/sha}",
      "updated_at": "2023-04-28T13:57:34Z",
      "url": "https://api.github.com/repos/kdysk000/github_actions_samples",
      "visibility": "public",
      "watchers": 0,
      "watchers_count": 0,
      "web_commit_signoff_required": false
    },
    "sender": {
      "avatar_url": "https://avatars.githubusercontent.com/u/102411958?v=4",
      "events_url": "https://api.github.com/users/kdysk000/events{/privacy}",
      "followers_url": "https://api.github.com/users/kdysk000/followers",
      "following_url": "https://api.github.com/users/kdysk000/following{/other_user}",
      "gists_url": "https://api.github.com/users/kdysk000/gists{/gist_id}",
      "gravatar_id": "",
      "html_url": "https://github.com/kdysk000",
      "id": 102411958,
      "login": "kdysk000",
      "node_id": "U_kgDOBhqutg",
      "organizations_url": "https://api.github.com/users/kdysk000/orgs",
      "received_events_url": "https://api.github.com/users/kdysk000/received_events",
      "repos_url": "https://api.github.com/users/kdysk000/repos",
      "site_admin": false,
      "starred_url": "https://api.github.com/users/kdysk000/starred{/owner}{/repo}",
      "subscriptions_url": "https://api.github.com/users/kdysk000/subscriptions",
      "type": "User",
      "url": "https://api.github.com/users/kdysk000"
    },
    "workflow": ".github/workflows/context_dump.yml"
  },
  "server_url": "https://github.com",
  "api_url": "https://api.github.com",
  "graphql_url": "https://api.github.com/graphql",
  "ref_name": "main",
  "ref_protected": false,
  "ref_type": "branch",
  "secret_source": "Actions",
  "workflow_ref": "kdysk000/github_actions_samples/.github/workflows/context_dump.yml@refs/heads/main",
  "workflow_sha": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  "workspace": "/home/runner/work/github_actions_samples/github_actions_samples",
  "action": "__run"
}
```