# NUnit HTML Report

This Github Action generates an HTML report from NUnit XML test results.

![](example.png)

## Usage

```yaml
on:
  pull_request:
  push:
jobs:
  test:
    name: Test 
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2
      - name: Run tests

      - name: Generate test report
        uses: rempelj/nunit-html-action@v1
        if: always()
        with:
          inputXmlPath: artifacts/results.xml
      - name: Upload test artifacts
        uses: actions/upload-artifact@v2
```

## License

The scripts and documentation in this project are released under the MIT License
