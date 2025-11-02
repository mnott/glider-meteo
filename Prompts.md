# Overview

Here are some prompts we've used to break down the original material. There were some challenges; first of all, the original PDF files were massive, so we had to compress them. Then, Claude Code does not like PDFs of too many pages, so we had to split them into chunks.
# Compression

You have PDFs of large size in the originals folder. I need you to use a command like

## Aggressive

```
/opt/homebrew/bin/gs \
 -sDEVICE=pdfwrite   \
 -dCompatibilityLevel=1.4 \
 -dPDFSETTINGS=/screen \
 -dColorImageDownsampleType=/Bicubic \
 -dColorImageResolution=36 \
 -dJPEGQ=50 \
 -dNOPAUSE \
 -dQUIET \
 -dBATCH \
 -sOutputFile=originals/meteo3_compressed.pdf originals/meteo3.pdf
```

## Less Aggressive

```
/opt/homebrew/bin/gs \
 -sDEVICE=pdfwrite   \
 -dCompatibilityLevel=1.4 \
 -dPDFSETTINGS=/screen \
 -dColorImageDownsampleType=/Bicubic \
 -dColorImageResolution=72 \
 -dJPEGQ=100 \
 -dNOPAUSE \
 -dQUIET \
 -dBATCH \
 -sOutputFile=originals/meteo3_compressed.pdf originals/meteo3.pdf
```

# Split into chunks

```
qpdf \
  --split-pages=50 \
  originals/meteo2_compressed.pdf \
  compressed/meteo2_compressed_part.pdf
```

# Analysis

## First Part

Pay attention to the header of the prompt. This needs to be adapted for the subsequent chunks.

```
For the following prompt, you are going to work on the Meteo Folder, Lesson 1, Part 1. Do not read other parts, as you would run out of context space because of the number of pages.

General Instructions:

- You are allowed to read pdf files in your subdirectories.
- You are allowed to generate the .md files as needed.

Your job is to generate some learning material.

For example, we might be on the Meteo topic, and we would have been asked to work on lesson 2. In this case, we would already have worked on lesson 1 before, so we can use the structural output of lesson 1 (the .md files) to inform us about the structure that we want to have.

If we were asked to work on lesson 1, we would not yet have a good example, so in that case, here is how we would have created those first files:

Go into the Meteo/compressed directory. Find the meteo1_qa_compressed.pdf file. Also find the meteo1_compressed_part*.pdf files. This is a lesson. I want you to

- read the qa file to understand the questions
- create, in the lesson1 directory, one .md file per topic which uses information from the meteo1 files 
- and breaks them down by topics per .md file following the structure of the PDFs. 
- We want our output files in English, with explanations of technical terms and qa in both languages.
- We want you to include all questions from the qa file in the appropriate topic
- If those questions are multiple choice, we want you to make sure that you indent them properly, so e.g. 
- A) ...
- B) ...  
- We want you to enrich your content with good explanations, making sure that all abbreviations are also explained.
- Give background, why any given concept is relevant, and be rather verbose than brief
- Feel free to include links to external resources like wikipedia and such
- Also feel free to add references to the PDF (parts) files (deep links with pages)
- If there are header numberings in the PDFs, recycle them in the .md so we have an easier way to match .md to .pdf
```


# Enrichment

```
Go to the Meteo/lesson3 folder.

Read all .md files. As you had generated them in chunks (see the prompt below), I want you to do another run across them and make sure they are appropriately split by topic.

I want you to also do an extra effort by

- adding good explanations, like be really rather verbose and don't just bullet point. Explain the why and what. Add anecdotes / good examples. Someone reading this material is a novice in the topic.
- making sure that all references to PDFs are correct (I may have moved some)
- Make sure definitions are near their use also. So yes you may have added a glossary, but then either link to it, or explain in context. For example, a sentence like "But METAR clouds are AGL!" is not really helpful unless we have links to the glossary.
- Make sure all links in the file that point to other files are correct (also within the related topics)
  
After that, in the same folder, you find a README. make sure it is complete - chances are, if we were working in chunks, only part of it is in there. You can read the .md next to it to ensure it is a comprehensive README.
```

# Update the Overall Readme

```
Go to the Meteo folder. In the subfolders (lesson*), you'll also find README files. I want you to generate an overall README that's meaningful and links to the lower level ones.
```

# Final Enrichment

```
Go to the Meteo folder. For all of those .md, I want you to make sure and really review critically, that they are understandable. If as a reader, you'd be confused somewhere, give more understandable context. We ultimately are creating a learning program here, and it has to include stories. If you feel that many of the files contain loads of bullet point lists, fine, you can keep them, but add some real text to them. Always read it out of the point of view of someone who's new in the topic. Do this for all files.

Also you'll find that there are lots of glossaries in the files. And elsewhere you may find abbreviations. Make sure you always have good links from those abbreviations to the glossaries.
```


# Re-Arrange Files

```
Thinking about it, I think we should re-arrange our files. In the compressed folder, we have like meteo1_compressed_part*.pdf and meteo1_qa_compressed.pdf. We should move those files to a subdirectory slides of lesson1, remove the _compressed_ part of the filename, do this for all lessons and then make sure that all file references in all .md files still remain correct.
```


# Make Github Compatible

```
We want to publish to Github. Make sure, all Obsidian links are converted to Github compatible links; you can keep the deep links to the PDF pages (convert them to Github format, but keep the references, as Github will ignore those).
```


# Let the Games Begin!

## Claude Code Format

```
I want you to read through Meteo/lesson1. Create a game to test my knowledge. Analyze the .md files, starting with the first, and figure out good questions/answers you'd like to ask. You're going to ask me the questions, and I'll answer. If my answer is good, you remove it from the list, if an answer needs improving, you explain and add it to be repeated later.

Let's focus on the first 2 .md files.
```

## Copilot Format

```
Create an adaptive quiz from the referenced note(s). Analyze all content and generate randomized questions covering:

- Basic recall & definitions
- Conceptual understanding
- Practical applications
- Analysis & reasoning

**Quiz Rules:**

- Start with random question from generated pool
- ✅ Correct answer → remove from list, next question
- ⚠️ Needs improvement → explain gaps, add to retry queue
- Include questions beyond those already in notes

**Reference Format:** For each question, provide: `[[note_title#Main Section]]` + brief location hint

**Question Style:**

- Present question only (no explanatory content)
- I'll answer, you evaluate
- Continue until all questions mastered or I say stop

Generate questions now and start the quiz!
```


---
<mark style="margin-top: 100; background-color: #3B3836; color: #494942">Created: `$=dv.span(dv.current().file.ctime)`</mark>