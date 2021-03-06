# Working with Project Tags in AWS CodeStar<a name="working-with-project-tags"></a>

You can associate tags with projects in AWS CodeStar\. Tags can help you manage your projects\. For example, you could add a tag with a key of `Release` and a value of `Beta` to any project your organization is working on for an upcoming beta release\.

## Add a Tag to a Project<a name="working-with-project-tags-add"></a>

1. With the project open in the AWS CodeStar console, in the navigation pane, choose **Project**\.

1. In the **Tags** area, for **Create new tag**, type the tag's name in the **Key** box\. Then type the tag's value in the **Value** box\.

1. Choose **Add tag**\.

## Remove a Tag from a Project<a name="working-with-project-tags-remove"></a>

1. With the project open in the AWS CodeStar console, in the navigation pane, choose **Project**\.

1. In the **Tags** area, for **Current tags**, find the tag you want to remove\.

1. In the **Options** column for that tag, choose **Remove**\.
**Note**  
You have approximately three seconds to undo the remove operation\. To keep the tag, choose **Undo**\.  
Otherwise, the tag is permanently deleted\.

## Get a List of Tags for a Project<a name="working-with-project-tags-list"></a>

Use the AWS Command Line Interface \(AWS CLI\) to run the AWS CodeStar `list-tags-for-project` command, specifying the name of the project\. For example:

```
aws codestar list-tags-for-project --id my-first-projec
```

If successful, a list of tags appears in the output, similar to the following:

```
{
  "tags": { 
    "Release": "Beta" 
  }
}
```