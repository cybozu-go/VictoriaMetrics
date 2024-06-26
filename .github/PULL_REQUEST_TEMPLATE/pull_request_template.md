### Describe Your Changes

Please provide a brief description of the changes you made. Be as specific as possible to help others understand the purpose and impact of your modifications.

### Checklist

The following checks are mandatory:

- [ ] I have read the [Contributing Guidelines](https://github.com/VictoriaMetrics/VictoriaMetrics/blob/master/CONTRIBUTING.md)
- [ ] All commits are signed and include `Signed-off-by` line. Use `git commit -s` to include `Signed-off-by` your commits. See this [doc](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work) about how to sign your commits.
- [ ] Tests are passing locally. Use `make test` to run all tests locally.
- [ ] Linting is passing locally. Use `make check-all` to run all linters locally.

Further checks are optional for External Contributions:

- [ ] Include a link to the GitHub issue in the commit message, if issue exists.
- [ ] Mention the change in the [Changelog](https://github.com/VictoriaMetrics/VictoriaMetrics/blob/master/docs/CHANGELOG.md). Explain what has changed and why. If there is a related issue or documentation change - link them as well.

  Tips for writing a good changelog message::

    * Write a human-readable changelog message that describes the problem and solution.
    * Include a link to the issue or pull request in your changelog message.
    * Use specific language identifying the fix, such as an error message, metric name, or flag name.
    * Provide a link to the relevant documentation for any new features you add or modify.

- [ ] After your pull request is merged, please add a message to the issue with instructions for how to test the fix or try the feature you added. Here is an [example](https://github.com/VictoriaMetrics/VictoriaMetrics/issues/4048#issuecomment-1546453726)
- [ ] Do not close the original issue before the change is released. Please note, in some cases Github can automatically close the issue once PR is merged. Re-open the issue in such case.
- [ ] If the change somehow affects public interfaces (a new flag was added or updated, or some behavior has changed) - add the corresponding change to documentation.


Examples of good changelog messages:

1. FEATURE: [vmagent](https://docs.victoriametrics.com/vmagent.html): add support for [VictoriaMetrics remote write protocol](https://docs.victoriametrics.com/vmagent.html#victoriametrics-remote-write-protocol) when [sending / receiving data to / from Kafka](https://docs.victoriametrics.com/vmagent.html#kafka-integration). This protocol allows saving egress network bandwidth costs when sending data from `vmagent` to `Kafka` located in another datacenter or availability zone. See [this feature request](https://github.com/VictoriaMetrics/VictoriaMetrics/issues/1225).

2. BUGFIX: [stream aggregation](https://docs.victoriametrics.com/stream-aggregation.html): suppress `series after dedup` error message in logs when `-remoteWrite.streamAggr.dedupInterval` command-line flag is set at [vmagent](https://docs.victoriametrics.com/vmgent.html) or when `-streamAggr.dedupInterval` command-line flag is set at [single-node VictoriaMetrics](https://docs.victoriametrics.com/).
