<p align="center">
  <img alt="golangci-lint logo" src="assets/go.png" height="150" />
  <h3 align="center">golangci-lint</h3>
  <p align="center">Fast linters runner for Go (navijation fork)</p>
</p>

---

This is a fork of [golangci-lint](https://github.com/golangci/golangci-lint) that aims to merge in all upstream changes as much
as possible while addressing some perceived issues that the upstream core maintainers consider
to be design choices. Please see the original repository for full and up-to-date
documentation. This README will be limited to changes from the upstream repository.


## Pass on Severities

This fork allows the CLI runner to exit with a zero return code if all open issues have severity
matching one of several configured options. The upstream supports assigning severities for
different issues. However, the CLI runner will exit non-zero regardless of the severity of issues,
which renders this feature rather "toothless".

`severity.pass-on-severities` can be configured to allow the CLI to pass on issues whose severities
match this set. There is no "ranking" of severities; only exact matches will be allowed.
