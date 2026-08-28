# Unit 03 — Links & Navigation

Welcome to **Unit 03: Links & Navigation**! This unit teaches you how to connect web pages using the Anchor tag (`<a>`), master absolute vs relative file paths, build internal page bookmarks, use special protocol links (`mailto:`, `tel:`), and apply security and accessibility best practices.

---

## 🎯 Unit Objective

By the end of this unit, you will be able to:
- Understand the core role of Hyperlinks (`<a>`) in Web Architecture and MERN routing.
- Differentiate between **Absolute URLs** (`https://...`) and **Relative File Paths** (`index.html`, `../about.html`, `./pages/contact.html`).
- Master window targets (`target="_blank"`, `target="_self"`) and security attributes (`rel="noopener noreferrer"`).
- Build **Internal Page Anchors** (`href="#section-id"`) for single-page bookmark navigation.
- Implement special protocol links: Email (`mailto:`), Telephone (`tel:`), SMS (`sms:`), and File Downloads (`download`).
- Write **Accessible Links** for screen readers (avoiding generic "Click Here" text).
- Avoid 404 broken link errors by mastering directory resolution trees.
- Answer top placement interview questions on HTML Links & Web Navigation.

---

## 📚 Topics Covered

1. **Introduction to Hyperlinks** (Role of `<a>` in web pages & frontend routing)
2. **The Anchor Tag & Syntax** (`<a>`, `href`, link text content)
3. **Absolute vs Relative File Paths** (Directory traversal, `./`, `../`, root `/`)
4. **Window Target & Security** (`target="_blank"`, `target="_self"`, Tabnabbing security, `rel="noopener noreferrer"`)
5. **Internal Page Navigation & Anchors** (`href="#id"`, single-page scrolling, jump-to-top links)
6. **Special Protocol Links** (`mailto:`, `tel:`, `sms:`, pre-filled email parameters)
7. **File Download Links** (`download` attribute, downloadable assets)
8. **Link Attributes & Tooltips** (`title`, `rel="nofollow"`, `rel="sponsored"`)
9. **Web Accessibility & SEO in Links** (Descriptive link text, screen reader accessibility, crawler indexing)
10. **Common Mistakes & Pitfalls** (Broken relative paths, missing `rel="noopener"`, "click here" text, unclosed `<a>` tags)
11. **Placement Interview Q&A** (Tabnabbing vulnerability, Absolute vs Relative, `mailto:` syntax)
12. **Quick Revision Table** (Cheat sheet summary)

---

## 📁 Files in This Unit

| File Name | Description |
|---|---|
| [notes.md](notes.md) | Comprehensive theory guide in natural Hinglish with technical accuracy and path diagrams. |
| [example_01_basic_links.html](example_01_basic_links.html) | Runnable HTML5 example for external links, `target="_blank"`, `rel="noopener noreferrer"`, `title`. |
| [example_02_relative_paths.html](example_02_relative_paths.html) | Runnable HTML5 example demonstrating relative file path navigation (`./`, `../`, child folders). |
| [example_03_page_anchors.html](example_03_page_anchors.html) | Runnable HTML5 example for single-page internal bookmark navigation (`#id`). |
| [example_04_special_links.html](example_04_special_links.html) | Runnable HTML5 example for `mailto:`, `tel:`, `sms:`, and `download` attributes. |
| [practice.md](practice.md) | 15 progressive practice questions (Level 1 to Level 4). |
| [practice_solutions.md](practice_solutions.md) | Complete runnable solutions and explanations for all 15 practice questions. |
| [mcqs.md](mcqs.md) | Exactly 20 multiple-choice questions with answers and detailed explanations. |

---

## 🗺️ Recommended Study Order

```
1. Read notes.md (Sections 1 to 4: Basics & Relative Paths)
       ↓
2. Open & inspect example_01_basic_links.html in Browser
       ↓
3. Open & inspect example_02_relative_paths.html in Browser
       ↓
4. Read notes.md (Sections 5 to 9: Anchors, Special Links, Security & A11y)
       ↓
5. Open & inspect example_03_page_anchors.html & example_04_special_links.html in Browser
       ↓
6. Read notes.md (Sections 10 to 12: Mistakes, Interview Q&A & Revision Table)
       ↓
7. Solve all questions in practice.md
       ↓
8. Verify code with practice_solutions.md
       ↓
9. Self-assess with 20 questions in mcqs.md
```

---

## 🏋️ Practice & MCQ Workflow

1. Read problem statements in [practice.md](practice.md).
2. Write your HTML solution in a new `.html` file inside your editor.
3. Test your link clicks in Google Chrome / Live Server.
4. Verify your code against [practice_solutions.md](practice_solutions.md).
5. Open [mcqs.md](mcqs.md), answer all 20 questions, and review explanations.

---

## ✅ Unit 03 Completion Checklist

Before moving to **Unit 04 (Images and Media)**, ensure you can check all of these:

- [ ] Do you know how to write a relative path to go UP one folder directory (`../`)?
- [ ] Can you explain why `rel="noopener noreferrer"` is required when using `target="_blank"`?
- [ ] Can you create an internal page anchor that jumps to a specific section `id` on the same page?
- [ ] Do you know how to write a `mailto:` link with a pre-filled subject line?
- [ ] Do you know why "Click Here" is a bad link text for web accessibility and SEO?
- [ ] Have you completed all 15 practice questions and verified with `practice_solutions.md`?
- [ ] Have you scored 16+ on `mcqs.md`?

---

*Ready? Open [notes.md](notes.md) to start Unit 03!* 🚀
