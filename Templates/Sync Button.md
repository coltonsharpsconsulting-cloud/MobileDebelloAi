<%*
const src = "_fit/.obsidian";
const dst = ".obsidian";
const files = app.vault.getFiles().filter(f => f.path.startsWith(src));
for (const file of files) {
  const destPath = file.path.replace(src, dst);
  const content = await app.vault.read(file);
  const existing = app.vault.getAbstractFileByPath(destPath);
  if (existing) {
    await app.vault.modify(existing, content);
  } else {
    await app.vault.create(destPath, content);
  }
}
new Notice("Config synced to .obsidian ✓");
%>
