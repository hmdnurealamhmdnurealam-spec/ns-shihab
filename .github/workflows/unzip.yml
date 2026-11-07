name: unzip
on: push
permissions:
  contents: write
jobs:
  unzip:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: |
          if [ -f files.zip ]; then
            unzip -o files.zip
            rm files.zip
            git config user.name "bot"
            git config user.email "bot@users.noreply.github.com"
            git add -A
            git commit -m "unzip files"
            git push
          fi
