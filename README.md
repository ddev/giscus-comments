# DDEV giscus-comments

This repository uses GitHub Discussions to store user comments via giscus.

## Moderation

To moderate comments, visit the [Discussions](https://github.com/ddev/giscus-comments/discussions) page, where you can filter by category.

## How to integrate giscus with your website

1. Choose the repository

   Ensure that the repository giscus will connect to meets the following requirements (This has already been done for `ddev/giscus-comments`):
    - The repository is [public](https://docs.github.com/en/github/administering-a-repository/managing-repository-settings/setting-repository-visibility#making-a-repository-public), otherwise visitors will not be able to view the discussion.
    - The [giscus](https://github.com/apps/giscus) app is installed, otherwise visitors will not be able to comment and react.
    - The Discussions feature is turned on by [enabling it for your repository](https://docs.github.com/en/github/administering-a-repository/managing-repository-settings/enabling-or-disabling-github-discussions-for-a-repository).

2. Create a discussion category

   [Create a new category](https://github.com/ddev/giscus-comments/discussions/categories/new) with:
   - A meaningful name
   - A description that explains how the comments will relate to the repository
   - The format set to `Open-ended discussion`

3. Generate the giscus script

   Visit [giscus.app](https://giscus.app/) and configure:
   - **Repository**: `ddev/giscus-comments`
   - **Page ↔️ Discussions Mapping**: Select "Discussion title contains page `<title>`"
   - **Discussion Category**: Choose the category created in step 2
   - **Features**:
     - Enable reactions for the main post
     - Place the comment box above the comments
     - Lazy-load the comments
   - **Theme**: If your site supports automatic light/dark mode, choose `Preferred color scheme`.

4. Embed the script to your website

    For example, the following script is used for the [ddev/addon-registry](https://github.com/ddev/addon-registry):

    ```js
    <script src="https://giscus.app/client.js"
            data-repo="ddev/giscus-comments"
            data-repo-id="R_kgDON5ODtA"
            data-category="Add-on registry comments"
            data-category-id="DIC_kwDON5ODtM4Cm8gG"
            data-mapping="title"
            data-strict="0"
            data-reactions-enabled="1"
            data-emit-metadata="0"
            data-input-position="top"
            data-theme="light"
            data-lang="en"
            data-loading="lazy"
            crossorigin="anonymous"
            async>
    </script>
    ```

5. Enjoy with new comments integration
