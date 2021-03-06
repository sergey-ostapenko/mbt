## mbt describe

Describe repository manifest

### Synopsis



`mbt describe branch [name] [--content] [--name <name>] [--fuzzy] [--graph] [--json]`<br>
Describe modules in a branch. Assume master if branch name is not specified.
Describe just the modules matching the `--name` filter if specified.
Default `--name` filter is a prefix match. You can change this to a subsequence
match by using `--fuzzy` option.

`mbt describe commit <commit> [--content] [--name <name>] [--fuzzy] [--graph] [--json]`<br>
Describe modules in a commit. Full commit sha is required.
Describe just the modules modified in the commit when `--content` flag is used.
Describe just the modules matching the `--name` filter if specified.
Default `--name` filter is a prefix match. You can change this to a subsequence
match by using `--fuzzy` option.

`mbt describe diff --from <commit> --to <commit> [--graph] [--json]`<br>
Describe modules changed between `from` and `to` commits.
In this mode, mbt works out the merge base between `from` and `to` and
evaluates the modules changed between the merge base and `to`.

`mbt describe head [--content] [--name <name>] [--fuzzy] [--graph] [--json]`<br>
Describe modules in current head.
Describe just the modules matching the `--name` filter if specified.
Default `--name` filter is a prefix match. You can change this to a subsequence
match by using `--fuzzy` option.

`mbt describe pr --src <name> --dst <name> [--graph] [--json]`<br>
Describe modules changed between `--src` and `--dst` branches.
In this mode, mbt works out the merge base between `--src` and `--dst` and
evaluates the modules changed between the merge base and `--src`.

`mbt describe local [--all] [--content] [--name <name>] [--fuzzy] [--graph] [--json]`<br>
Describe modules modified in current workspace. All modules in the workspace are
described if `--all` option is specified.
Describe just the modules matching the `--name` filter if specified.
Default `--name` filter is a prefix match. You can change this to a subsequence
match by using `--fuzzy` option.

### Output Formats

Use `--graph` option to output the manifest in graphviz dot format. This can
be useful to visualise build dependencies.

Use `--json` option to output the manifest in json format.



### Options

```
      --graph   Format output as dot graph
  -h, --help    help for describe
      --json    Format output as json
```

### Options inherited from parent commands

```
      --debug       Enable debug output
      --in string   Path to repo
```

### SEE ALSO
* [mbt](mbt.md)	 - mbt - The most flexible build orchestration tool for monorepo
* [mbt describe branch](mbt_describe_branch.md)	 - 
* [mbt describe commit](mbt_describe_commit.md)	 - 
* [mbt describe diff](mbt_describe_diff.md)	 - 
* [mbt describe head](mbt_describe_head.md)	 - 
* [mbt describe intersection](mbt_describe_intersection.md)	 - 
* [mbt describe local](mbt_describe_local.md)	 - 
* [mbt describe pr](mbt_describe_pr.md)	 - 

###### Auto generated by spf13/cobra on 16-Jun-2018
