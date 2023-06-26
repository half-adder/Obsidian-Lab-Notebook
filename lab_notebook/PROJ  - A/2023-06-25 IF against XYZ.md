---
start_date: 2023-06-25
end_date:
id: 3D1E0511
status: done
tags: [experiment]
---

# Purpose

This experiment file is generated using a template (template is located [[experiment-template|here]], you can edit it to your liking). In this section I normally describe the reason/rationale for doing what I'm doing. Right now, I'll explain a little about how I use the lab notebook.

Each experiment file doesn't necessarily correspond to a single "experiment". I think of each file as corresponding to its own little mini "project". So for example, each of the following would get a single "experiment" file:

- Cloning a new plasmid
- Creating a CRISPR mutant fly
- Doing a lifespan on a set of 4 strains
- Doing CUT&RUN on a set of 3 strains, with 4 antibodies each

Of course, you will have to decide how your personal notebook is atomized.

In any case, each "experiment" gets a single file (like this one here), which starts with a `YYYY-MM-DD` date, indicating the day that I made the file, so that in the filesystem, each experiment is sorted by start date.

## Metadata

At the top of the file you will see some metadata. These are simply key-value pairs that encode general information about this experiment, to make finding it easier later on. I keep track of start and end date, the status ("in-progress", "failed", "done"), any tags that might be relevant ("genomics", "cloning", "behavior", "lifespan", "IF"). 

I also generate a unique ID for each experiment. The thought here is that I could write that ID on a plate, tube, etc., and ctrl-F my lab notebook for that short string, and it should only come up once: in the experiment that I was working on for that tube, plate, etc.

## Daily Entries

The last top-level section is the "Entries" section. When I start work on an "experiment", I write down what I did that day under  `YYYY-MM-dd` header. I made a shortcut to generate this header quickly. On a mac, type `⌘-P` (on Windows, `Ctrl-P`), then type "New Daily Entry on Current Experiment" (you don't have to type the whole thing, just the first couple of letters is enough to autocomplete). Pressing enter on the selection will add a line to the end of the file with a new header with the current date.

## Task Management

Whenever I have something to do for the current experiment, I write it in the file.

- [ ] Like this 📅 2023-06-26 

Obsidian indexes all To-Dos and allows you to collect them with various filters and groupings, for example: Due date, file of origin, tag (see [here](https://publish.obsidian.md/tasks/Introduction) for complete documentation).

You'll notice the `# Tasks` header. Under that is all of the tasks in the current file.

To see all tasks from all experiments, go to the [[Dashboard]].

# Tasks

```dataviewjs
function callout(text, type) {
    const allText = `> [!${type}]\n` + text;
    const lines = allText.split('\n');
    return lines.join('\n> ') + '\n'
}

const query = `
not done
path includes ${dv.current().file.path}
# you can add any number of extra Tasks instructions, for example:
group by due
`;

dv.paragraph(callout('```tasks\n' + query + '\n```', 'todo'));
```

# Entries

## 2023-06-24

Here's an example entry.

You can add pictures to your experiment files, for example of gels that you ran.

![[2023-06-25_GEL_description-of-the-gel.jpg|200]]

You can use `[[filename|width]]` syntax to make the image fit in the page a little nicer. I like to use `200` as the width. Clicking on the image brings it to full size.

## 2023-06-25

Another example entry.

- [ ] Here's an example task  📅 2023-06-26 
- [ ] Another task 📅 2023-06-27 