# Recovery file from uncommitted after git reset hard

## Let's go

#### Firstly, run this command to list all unreachable blobs:

```bash
$ git fsck --cache --unreachable $(git for-each-ref --format="%(objectname)") > all
```

In which case you can see those objects with:

```text
unreachable blob 14ac56f85a5852690796785cdd82636ca358fd56
unreachable blob 83f0c362c9ea808dc18a5d6638ea65ac02e008d6
unreachable blob b369f3137873e72cbb55df25a0832f0036c6a3dd
unreachable blob c069b0e9b518852269e8af96dda25e50bd2d946b
unreachable blob 212ea9a0866d30469917fea867db6dff9dfb23ee
```

#### Secondly, you can restore file with command:

```text
$ git show b369f3137873e72cbb55df25a0832f0036c6a3dd > contents
```



