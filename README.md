1. Add this to your ~/.zshrc

```bash
md2pdf () {
        pandoc --standalone -c ~/.pandoc/github-markdown.css -f gfm -t html $1 > out.html && weasyprint out.html out.pdf && rm out.html && open out.pdf
}
```

2. Install weasyprint and pandoc with your favorite package manager.

3. Copy the contents of `.pandoc` to `~/.pandoc` (creating if not exists).

4. Source your ~/.zshrc

5. Use `md2pdf README.md` to generate the PDF.
