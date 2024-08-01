# Commit 信息规范

这些术语通常用于 Git 提交信息中，以描述不同类型的更改。它们是基于 [Conventional Commits](https://www.conventionalcommits.org/) 规范的。以下是每个术语的含义：

1. **build**: 与构建系统或外部依赖项相关的更改（如构建脚本、依赖包、生成的文件）。

   - 示例: `build: update webpack configuration`

2. **chore**: 日常事务性工作，通常不会修改源代码或测试文件（如更新工具、配置文件）。

   - 示例: `chore: update npm scripts`

3. **ci**: 持续集成配置的更改（如 Travis、Circle、Jenkins、GitLab CI 等 CI 配置文件的更改）。

   - 示例: `ci: update Travis CI configuration`

4. **docs**: 文档的更改（如 README、API 文档、注释）。

   - 示例: `docs: add contribution guide`

5. **feat**: 新功能的引入。

   - 示例: `feat: add user login functionality`

6. **fix**: 修复 bug。

   - 示例: `fix: correct header alignment issue`

7. **perf**: 提升性能的更改。

   - 示例: `perf: improve page load speed by optimizing images`

8. **refactor**: 代码重构，既不修复 bug 也不添加新功能的代码更改。

   - 示例: `refactor: simplify user authentication logic`

9. **revert**: 撤销先前的提交。

   - 示例: `revert: revert commit 1234567`

10. **style**: 代码风格的更改（如缩进、空格、格式化），不影响代码功能。

    - 示例: `style: format code with prettier`

11. **test**: 添加或修改测试。
    - 示例: `test: add unit tests for user service`

使用这些术语可以帮助项目维护人员和其他开发人员快速了解每次提交的目的和影响，从而提高代码审查和项目管理的效率。

# 遇到的一些报错

## 问题 1 - `npx imooc-jira-tool` 执行报错

```shell
$ npx imooc-jira-tool
npm error could not determine executable to run
npm error A complete log of this run can be found in: /Users/xxx/.npm/_logs/2024-08-01T13_44_35_553Z-debug-0.log
```

解决办法：

```shell
$ npm install jira-dev-tool
$ npx msw init ./public
```

其实就是将执行命令 `imooc-jira-tool` 的自动化过程手动自己执行一下。猜测问题是 `npx` 无法找到 `imooc-jira-tool` 这个包的可执行文件（who knows?）。
