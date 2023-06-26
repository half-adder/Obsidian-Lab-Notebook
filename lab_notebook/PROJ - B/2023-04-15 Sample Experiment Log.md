---
start_date: 2023-06-25
end_date:
id: 3CED050D
status: in-progress
tags: [experiment]
---

# Purpose

This is where you can describe the background of your experiment, why you're doing it, etc.

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

## 2023-06-25

Here's a sample entry. You can add pictures of your gels, or whatever else.

To start a new day, simply use the shortcut "QuickAdd - New Daily Entry on Experiment"

### Line of work A

Sometimes I am working on multiple things in the course of one "Experiment". For example, PCRing a bunch of fragments for a Gibson assembly. In that case, I might be optimizing different fragments on different days. I use these `###` headers to indicate which piece I'm working on.

### Line of work B

That allows me to keep track of things a bit nicer.

Also, when I generate things to do, I go ahead and add the task directly to my lab notebook. All the tasks for this document are collected at the top.

Also, all tasks in the lab notebook are collected in the [[Dashboard]].

- [ ] Example Task 📅 2023-06-26 

## 2023-06-26

### Line of work A

So then here I can take notes on A again.
