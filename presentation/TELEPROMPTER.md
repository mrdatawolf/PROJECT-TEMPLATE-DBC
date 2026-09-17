# Talk teleprompter

Open `index2.html` in a browser. When opening directly from disk, use **Load .md
files** to select all Markdown files in `presentation/Talk` (Ctrl+A in that
folder). Files are read locally, without uploading them. When served over HTTP,
the page automatically loads `Intro.md` and `p1.md` through `p26.md`.

All selected files become **one continuous talk**, ordered Intro, p1, p2, …,
p26. You do not need to combine or move the source files. Each file starts with
a prominent separator labeled **Page N of 27 — filename**.

Use **Previous page / Next page** or **Left / Right arrow** to move between
files, or choose any page from the Section menu. The page counter and menu track
your reading position as you scroll. Jumping pauses playback; press Start to
resume. To load the whole talk from disk, select **all** the Talk `.md` files
together in the picker, rather than opening them one at a time.

Press **Start** or **Space** to scroll or pause. Use **+ / −**, the speed slider,
or **Up / Down** to adjust pixels per second. Text size, section navigation,
restart (**Home**), and full screen are available in the toolbar. Keyboard
shortcuts apply when focus is outside the toolbar controls; click the talk text
to return focus to the reading area. Manual scrolling and hiding the browser tab
pause playback. Playback stops at the end.

The page supports headings, paragraphs, emphasis, inline code, and separators;
it preserves other Markdown as readable source text. It has no external runtime
dependencies. Reload or reselect files after editing the talk. When adding new
sections, extend `talkFiles` in `index2.html` for automatic HTTP loading, or use
the file picker, which sorts Intro first and p files numerically.
