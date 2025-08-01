# docusaurus-paginator-fix

This patch changes the default layout of the Docusaurus `BlogPostPaginator` component to match a more intuitive navigation flow:

- The **left** side shows the **"Previous"** (older) post  
- The **right** side shows the **"Next"** (newer) post

This layout is more consistent with:

- General UI/UX conventions (e.g. pagination, horizontal scrolling)
- Natural reading flow in left-to-right languages
- Other parts of Docusaurus, such as documentation navigation

---

## 🖼️ Before & After

Here’s how the paginator looks **before and after** applying this patch:

<table>
  <tr>
    <td align="center"><strong>🔙 Default layout (before)</strong></td>
    <td align="center"><strong>✅ Patched layout (after)</strong></td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/gumi278/docusaurus-paginator-fix/main/screenshots/before.png" width="400" alt="Default paginator layout (before)">
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/gumi278/docusaurus-paginator-fix/main/screenshots/after.png" width="400" alt="Patched paginator layout (after)">
    </td>
  </tr>
</table>


## 🔧 How to apply this patch

1. Copy the component file into your own Docusaurus project:

```sh
mkdir -p src/theme/BlogPostPaginator
curl -o src/theme/BlogPostPaginator/index.tsx https://raw.githubusercontent.com/gumi278/docusaurus-paginator-fix/main/src/theme/BlogPostPaginator/index.tsx
```


2. Rebuild your Docusaurus site:

```sh
npm run build
```

3. Then serve the site locally:

```sh
npm run serve
```

You should now see the "Previous" post on the left, and the "Next" post on the right!

---

## 📎 Notes

* This override uses [Docusaurus theme swizzling](https://docusaurus.io/docs/using-themes#theme-swizzling), which is the official way to customize theme components.
* Tested with:

  * Docusaurus version: `3.8.1`
  * Node.js version: `22.17.0`

---

## 💡 Feedback & Contributions

Issues and pull requests are welcome!
If you encounter any problems or want to suggest improvements, feel free to open an issue or discussion.

---

## 📄 License

This patch is released under the [MIT License](./LICENSE).
