<!--
 * @Author: lidi10@staff.weibo.com
 * @Date: 2024-04-30 20:03:41
 * @LastEditTime: 2024-04-30 20:55:22
 * @LastEditors: lidi10@staff.weibo.com
 * @Description: 
 * Copyright (c) 2023 by Weibo, All Rights Reserved. 
-->
# Contributing

## Setup
```bash
git clone https://github.com/chuangyeshuo/sqlvana
cd sqlvana/

python3 -m venv venv
source venv/bin/activate

# install package in editable mode
pip install -e '.[all]' tox pre-commit

# Setup pre-commit hooks
pre-commit install

# List dev targets
tox list

# Run tests
tox -e py310
```

## Running the test on a Mac
```bash
tox -e mac
```

## Do this before you submit a PR:

Find the most relevant sample notebook and then replace the install command with:

```bash
%pip install 'git+https://github.com/chuangyeshuo/sqlvana@your-branch#egg=vanna[chromadb,snowflake,openai]'
```

Run the necessary cells and verify that it works as expected in a real-world scenario.
