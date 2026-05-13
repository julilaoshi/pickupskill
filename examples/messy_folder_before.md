# Messy Folder Before Cleanup

This is a synthetic example. It does not represent a real user's folder.

```text
root/
  IMG_0042.png
  IMG_0043.png
  final_export.mp4
  final_export.srt
  final_export_thumbnail.png
  brand_logo.ai
  brand_logo_preview.png
  meeting_notes.txt
  invoice_maybe.pdf
  random_reference.jpg
  website_project/
    package.json
    package-lock.json
    src/
    public/
  article_draft.docx
  article_refs/
    paper_a.pdf
    paper_b.pdf
  old_empty_folder/
```

## First Read

- `website_project/` looks like a software project package.
- `final_export.mp4`, `final_export.srt`, and `final_export_thumbnail.png` look like one media export group.
- `brand_logo.ai` and `brand_logo_preview.png` look like one design group.
- `article_draft.docx` and `article_refs/` may be related but should not be forced without confirmation.
- `invoice_maybe.pdf` is ambiguous.
- `old_empty_folder/` should not be deleted by default.

## Cautious Plan

```text
safe moves:
  final_export.mp4 -> media/final_export/
  final_export.srt -> media/final_export/
  final_export_thumbnail.png -> media/final_export/
  brand_logo.ai -> design/brand_logo/
  brand_logo_preview.png -> design/brand_logo/
  IMG_0042.png -> review-images/
  IMG_0043.png -> review-images/
  random_reference.jpg -> references/

keep in place:
  website_project/

review bucket:
  invoice_maybe.pdf
  article_draft.docx
  article_refs/
  old_empty_folder/
```

