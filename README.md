# James Bateson Unseen Group dashboard task
Task for Unseen Group dashboard page design and build

## Design

### Research and initial prep

I started off by having a look at the current TopScore site to get an idea of their branding.

I then jotted down some ideas for how I interpreted the breif, and how I planned to appraoch it, tools I thought I would use etc. You can find some pictures of these files in the `dashboard-design` directory. Whilst they are rough and not moview quality. I think it shows an important part of the process and how I like to appraoch tasks.

### Moving into Figma

Once I have a clear idea based on my research, notes and rough wireframe sketch, I moved into building this out in Figma.

Here is the link to the Figma project: https://www.figma.com/design/o32WULxi7A1plaXmGHgGHW/Unseen-Group-task?node-id=1-2&t=3QsCdyazc4NIvqTd-1

There are a few things I would like to note from the design. Things with more time, more context of the project etc I may have done differently.

* I did not include the header and footer in the design. I have however added some basic versions of these in the build
* The assessor averages section really got me thinking! There's potential for a heck of a lot of data to be in there, and to be honest I'm not sure I came up with the best solution. It's something that I would look to test and get feedback on from people using it in a project
    * My main aim was to split the data out to make it easier to consume. However, with my first solution, with a lot of assessors there could potentially be 13 or so big tables, which would take up a lot of space (this is the solution I built in the end)
    * In the design I have also shown a solution that could help with the size of these tables and this solution. This would be to just view the average scores of one assesor at a time. The downside to this being that you would lose the ability to do any comparison. however, again would want to find out if people were using the data in that kind of way
    * A final thought I had (but didn't design or build) was to have one large table as on the provided current dashboard, and have the ability to "stick" the assessor name column, so people could have this in view at all times and then just horizontally scroll to see the different criteria scores
* To speed up the design process I used some components from the Simple Design System Figma library and then adapted them for use. Probably not the best way to go about things, but with no assests/brand guidelines and the time factor, I decided this would be more efficient

## Build

All the code build work can be found in the `dashboard-build` directory, and a preview of the page can be seen at: https://jb-unseen-group-task.netlify.app/ (just a quick netlify site I added)

If you want to run the project locally, it's built with Astro and Tailwind. I chose Astro as I have used it before, and it allows flexibility of approach which I wasn't 100% on.

To run locally:

* Clone
* From the project root in your terminal `cd dashboard-build`
* `npm i`
* `npm run dev` 

As witht he design there are a few things I would have done differently and extra with more time:

* The project switching and filters do not work (although can interesct with the elements)
* The mobile navigation toggle does not work
* I have organised my code into components for each section and in the case of the tables, smaller chunks. With more time this would have allowed me to add some dynamic functionality around these, add some mock data and logic, making less markup with loops and passing in props etc. Apologies if this is what you were expecting to see in this task.
* I have used native date inputs for the datepickers, however, there are known accessibility issues with these, such as keyboard date selection. With more time I would have looked into accessibility packages there may be out there making them a more custom element
