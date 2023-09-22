<template>
    <div class="main-content">
      <breadcumb :page="'Roles & Permissions'" :folder="'Users'" :folder2="'Roles and Permissions'" />
     
    </div>
</template>
  
<script>
export default {
metaInfo: {
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "Task Manager",
},
data() {
    return {
    columns: [
        {
        label: "Name",
        field: "name",
        },
        {
        label: "Span",
        field: "span",
        html: true,
        },
        {
        label: "Created On",
        field: "createdAt",
        type: "date",
        dateInputFormat: "yyyy-mm-dd",
        dateOutputFormat: "MMM Do yy",
        },
        {
        label: "Percent",
        field: "score",
        type: "percentage",
        },
        {
        label: "Button",
        field: "button",
        html: true,
        tdClass: "text-right",
        thClass: "text-right",
        },
    ],
    rows: [
        {
        id: 1,
        name: "John",
        span: '<span class="badge badge-primary">Primary</span>',
        createdAt: "2019-10-29",
        score: 0.03343,
        },
        {
        id: 2,
        name: "Jane",
        span: '<span class="badge badge-danger">Primary</span>',
        createdAt: "2011-10-31",
        score: 0.03343,
        },
        {
        id: 3,
        name: "Susan",
        span: '<span class="badge badge-warning">Primary</span>',
        createdAt: "2011-10-30",
        score: 0.03343,
        },
        {
        id: 4,
        name: "Chris",
        span: '<span class="badge badge-primary">Primary</span>',
        createdAt: "2011-10-11",
        score: 0.03343,
        },
        {
        id: 5,
        name: "Dan",
        span: '<span class="badge badge-danger">Primary</span>',
        createdAt: "2011-10-21",
        score: 0.03343,
        },
        {
        id: 6,
        name: "John",
        span: '<span class="badge badge-success">success</span>',
        createdAt: "2011-10-31",
        score: 0.03343,
        },
        {
        id: 1,
        name: "John",
        span: '<span class="badge badge-warning">Warning</span>',
        createdAt: "2019-10-29",
        score: 0.03343,
        },
        {
        id: 2,
        name: "Jane",
        span: '<span class="badge badge-info">Info</span>',
        createdAt: "2011-10-31",
        score: 0.03343,
        },
        {
        id: 3,
        name: "Susan",
        span: '<span class="badge badge-dark">Dark</span>',
        createdAt: "2011-10-30",
        score: 0.03343,
        },
        {
        id: 4,
        name: "Chris",
        span: '<span class="badge badge-warning">Warning</span>',
        createdAt: "2011-10-11",
        score: 0.03343,
        },
        {
        id: 5,
        name: "Dan",
        span: '<span class="badge badge-info">Info</span>',
        createdAt: "2011-10-21",
        score: 0.03343,
        },
        {
        id: 6,
        name: "John",
        span: '<span class="badge badge-primary">Primary</span>',
        createdAt: "2011-10-31",
        score: 0.03343,
        },
    ],
    };
},
methods: {
    addFile() {
    // console.log("hello");
    },
},
};
</script>
<style></style>
