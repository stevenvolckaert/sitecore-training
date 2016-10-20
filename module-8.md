<p align="center">
    <a href="module-7.md">← Module 7</a> | <strong>Module 8</strong> | <a href="module-9.md">Module 9 →</a>
</p>

# Module 8: Dealing with Your Data

## 8.1 Item Buckets

Some items don't need to be stored in a tree structure (the Sitecore default). Item buckets satisfy this void.

In Content Editory, right-click the gutter, and enable **Item Buckets**. The items in a bucket will **not** display in
the Content Tree - you need to use the search functionality to find them! Alternatively, click **View** on the ribbon,
and enable **Buckets**. They'll then display in the Content Tree. However, remember to switch the view off, because this
does have an impact on performance!

Items need to be 'bucketable' to be put into a bucket when a folder is converted to a bucket. The 'bucketable' is a
boolean flag on an item. this flag is a so-called 'Standard Field'. To see it, go to View tab, and enable **Standard
Fields**.

Any item can become a bucket. To bucket an item, it's **Bucketable** flag must be set, **AND** its parent item needs to
be a bucket. You can inherit the `bucketable` base template, which has the flag correctly set.

After making changes to the bucketability of items in a bucket, *sync* the bucket!

### Facets

Facets allow one to 'narrow-down' (filter) search results.

* Facets are persisted in `<master>/sitecore/system/Settings/Buckets/Facets/`.

## 8.2 Search

* You can use the search box at the top to filter the results. The search meachanism can be replicated in code (queries
  an index instead of a tree).
* Wildcards are supported (not demo-ed).
* Use Custom search to find some things (unknown) - e.g.
* *Tip: See Sitecore Documentation to learn to use the search box!*

~~~
// Using the Sitecore Search functionality from code
// Sitecore will automatically create the correct index (the index of the context's database).
var indexableItem = new SitecoreIndexableItem(Sitecore.Context.Item);
var index = ContentSearchManager.GetIndex(indexableItem);

using (var context = index.CreateSearchContext())
{
    var q = context.GetQueryable<SearchResultItem>()
        .Where(x => x["Page Heading"].Contains("b"))
        .Where(x => x.Language == Sitecore.Context.Language.Name)
        .Where(x => x.Paths.Contains(new ID("{<GUID>}");
        //.Where(x => x.Path.StartsWith("your-search-string");

    repeaterResults.DataSource = q.ToList();
    repeaterResults.DataBind();
}
~~~

* Use the `IndexFieldAttribute` on .NET classes to be able to easily access the search API programmatically.

<p align="center">
    <a href="module-7.md">← Module 7</a> | <strong>Module 8</strong> | <a href="module-9.md">Module 9 →</a>
</p>
