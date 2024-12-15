# VS Code "Stage Selected Ranges" Issue Reproduction

This is a repro of some issues described in this [VS Code
issue](https://github.com/microsoft/vscode/issues/235904).

## Steps

1. Clone this repo and open it in VS Code
2. In [file.html](file.html), make a change on line 17
3. Select lines 16-18 which contain that change
4. Choose "Git: Stage Selected Ranges" from the command palette
   - You can see the change is staged without issue
4. Now make a change on line 27
5. Select lines lines 26-28
6. Choose "Git: Stage Selected Ranges" again
   - Now you can see unexpected changes are staged

## Screenshots following these steps

<details>

<summary>Selection before staging the first change</summary>

![Selection before staging the first change](1.png)

</details>

<details>

<summary>Diff of the first staged change</summary>

![Diff of the first staged change](2.png)

</details>

<details>

<summary>Selection before staging the second change</summary>

![Selection before staging the second change](3.png)

</details>

<details>

<summary>Diff after both changes should have been staged</summary>

![Diff of the second staged change](4.png)

</details>

<details>

<summary>Diff of remaining unstaged changes</summary>

![Diff of the remaining unstaged changes](5.png)

</details>

