# amirhosseinmollaei.github.io

Personal academic website for Amirhossein Mollaei, PhD student in Mechanical
Engineering at Lehigh University.

Live at <https://amirhosseinmollaei.github.io>.

Built with [Academic Pages](https://github.com/academicpages/academicpages.github.io),
a fork of the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
Jekyll theme. GitHub Pages rebuilds the site automatically on every push to
`master`.

## Where things live

| What | Where |
|---|---|
| Homepage text, news, education, teaching | `_pages/about.md` |
| Publications, one file per paper | `_publications/` |
| Research pages with demo videos | `_portfolio/` |
| Header menu | `_data/navigation.yml` |
| Site and sidebar settings | `_config.yml` |
| CV, demo videos, other downloads | `files/` |
| Headshot and icons | `images/` |

## Common edits

**Add a news item.** Open `_pages/about.md`, find the `## News` list, and add a
line at the top in the same format:

```markdown
- **[Mon YYYY]** What happened.
```

**Add a paper.** Copy any file in `_publications/` to a new one named
`YYYY-MM-DD-short-slug.md` and edit the fields at the top. Use
`category: conferences` for accepted papers and `category: manuscripts` for
work under review.

**Add a demo video.** Drop the `.mp4` into `files/`. The pages are already
wired for these names, so a file dropped in with the right name appears on the
site by itself:

| Paper | Filename to use |
|---|---|
| Active NBV for Risk-Averse Path Planning (ICRA 2026) | `files/nbv-risk-averse.mp4` (present) |
| Conflict-Aware Active Perception (CDC 2026) | `files/caap.mp4` (present) |
| SemSafe-3DGS (SeMaNa / IROS 2026) | `files/semsafe.mp4` |
| Splat-CBF (preprint) | `files/splatcbf.mp4` |

Keep clips under about 20 MB. GitHub refuses any file over 100 MB, and the
whole repository is what GitHub Pages serves.

To use a clip on a new page:

```liquid
{% include demo-video.html src="yourclip.mp4" caption="Optional caption." %}
```

The player only appears once the file is actually in `files/`; until then the
page shows a visible TODO box instead of an empty video element. If a matching
`yourclip-poster.jpg` is present it is used as the poster frame.

**Replace the headshot.** Overwrite `images/profile.png`.

## Note on the front matter

The block between the `---` lines at the top of each Markdown file is YAML, and
it is whitespace-sensitive. If a build fails right after an edit, the cause is
almost always a stray space or an unquoted colon in the file that was just
changed.
