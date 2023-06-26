---
start_date: <% tp.date.now() %>
end_date:
id: <% tp.user.now_adler32() %>
status: in-progress
tags: [experiment]
---

# Purpose

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus hendrerit iaculis ligula eget maximus. Nunc quis risus imperdiet, sodales mauris nec, aliquam dui. Morbi convallis mattis ligula sed efficitur. Maecenas ac massa odio. Quisque non enim porta, blandit velit nec, varius ante. Duis risus leo, tempor ut purus quis, sagittis consequat mi. Morbi suscipit massa non nisi tincidunt ornare. Aenean justo sem, blandit non lacinia et, commodo at dolor. Interdum et malesuada fames ac ante ipsum primis in faucibus. Ut laoreet interdum nisl at pretium.

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

## <% tp.date.now() %>