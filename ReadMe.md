# ModLinks

This is the repository that holds information on every public mod that should be accessible via mod installers.

## What ModLinks is for

ModLinks is for mods of the game Hollow Knight (2017) by Team Cherry.

## How to add/update a mod to ModLinks

### Easy/Recommended Approach
1. Go to https://github.com/hk-modding/modlinks/blob/main/ModLinks.xml
1. Click the pencil at the top right corner
1. Make the changes, scroll to the top and click "Commit Changes"
1. Fill out the commit info and click the button that says "Propose Changes."
1. Allow GitHub to create a fork, branch, and pull request for you.

### Traditional Approach

If you are familiar with common Git and GitHub workflows, this approach may be more familiar to you. If you are not, you are strongly advised to use the approach outlined above.
1. Create a fork of this repo. If you already have a fork, sync the main branch from parent instead.
1. Clone/pull your fork
1. Create a new branch from main and check it out
1. Make the changes and commit them
1. Push to your branch on your fork
1. Create a pull request to upstream

### What maintainers look for in order to merge

Maintainers of ModLinks look for the following before merging the manifest of a new mod into ModLinks:
- Source Code available in a git repository
  - Not necessarily hosted on github.com
- The mod is not malware
  - Kind of self-explanatory
- The mod is for the same age groups as Hollow Knight itself also is
- The mod is not of another person
  - it needs more than minimal modifications
  - unless a good faith attempt has been made to contact the original author

## Example manifest

```xml
<Manifest>
    <Name>Test Name</Name>
    <DisplayName>Test Name that is used for display, where &lt;Name&gt; can be used as a sort of ID</DisplayName>
    <Description>Test description</Description>
    <Version>0.0.0.0</Version>
    <Links>
        <Linux SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://linux.link]]></Linux>
        <Mac SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://mac.link]]></Mac>
        <Windows SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://windows.link]]></Windows>
    </Links>
    <Link SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://multiplatform.link]]></Link>
    <Dependencies>
        <Dependency>Another mod's name that this mod depends on</Dependency>
    </Dependencies>
    <Repository>
        <![CDATA[https://github.com/user/repo]]>
    </Repository>
    <Issues>
        <![CDATA[https://website/for/bug_reports]]>
    </Issues>
    <Integrations>
        <Integration>Another mod's name, like the dependency list, but not a hard dependency, but extra stuff when it is installed alongside</Integration>
    </Integrations>
    <Tags>
        <Tag>Either of: Accessibility/Boss/Charm/Cosmetic/Expansion/Gameplay/Joke/Library/Optimization/Utility</Tag>
    </Tags>
    <Authors>
        <Author>An author's name. Has no specific format.</Author>
    </Authors>
</Manifest>
```
