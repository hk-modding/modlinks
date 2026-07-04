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
    <!-- REQUIRED: this will be used as the foldername the mod is stored in, inside the game files -->
    <Name>TestName</Name>
    <!-- OPTIONAL: Name that is used for display, like in mod installers, where <Name> can be used as a sort of ID -->
    <DisplayName>Test Name</DisplayName>
    <!-- REQUIRED: Used in mod installers -->
    <Description>Test description</Description>
    <!-- REQUIRED: Used for update checks -->
    <Version>0.0.0.0</Version>
    <!-- REQUIRED: Either `Links` OR `Link`, not both, not neither. SHA256 is the sha256 of the actual file that is downloaded -->
    <Links>
        <Linux SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://linux.link]]></Linux>
        <Mac SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://mac.link]]></Mac>
        <Windows SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://windows.link]]></Windows>
    </Links>
    <Link SHA256="0000000000000000000000000000000000000000000000000000000000000000"><![CDATA[https://multiplatform.link]]></Link>
    <!-- REQUIRED: at minimum `<Dependencies />`, but if needed with one or more mod's names in it. Here are some Library mods as examples -->
    <Dependencies>
        <Dependency>FrogCore</Dependency>
        <Dependency>HKMirror</Dependency>
        <Dependency>MagicUI</Dependency>
        <Dependency>Osmi</Dependency>
        <Dependency>Satchel</Dependency>
        <Dependency>SFCore</Dependency>
        <Dependency>Vasi</Dependency>
        <Dependency>WeaverCore</Dependency>
    </Dependencies>
    <!-- REQUIRED: where can the code for the mod be found? -->
    <Repository>
        <![CDATA[https://github.com/user/repo]]>
    </Repository>
    <!-- OPTIONAL: where should issues with the mod be reported? -->
    <Issues>
        <![CDATA[https://website/for/bug_reports]]>
    </Issues>
    <!-- OPTIONAL: Optional dependencies can be listed here. Things, where extra stuff happens when it is installed alongside. -->
    <Integrations>
        <Integration>Randomizer 4</Integration>
    </Integrations>
    <!-- OPTIONAL: How would the mod be described with a set of Tags? Any combination of the following: -->
    <Tags>
        <Tag>Accessibility</Tag>
        <Tag>Boss</Tag>
        <Tag>Charm</Tag>
        <Tag>Cosmetic</Tag>
        <Tag>Expansion</Tag>
        <Tag>Gameplay</Tag>
        <Tag>Joke</Tag>
        <Tag>Library</Tag>
        <Tag>Optimization</Tag>
        <Tag>Utility</Tag>
    </Tags>
    <!-- OPTIONAL: Who made the mod or was part in creating it? -->
    <Authors>
        <Author>An author's name. Has no specific format.</Author>
        <Author>Second person</Author>
    </Authors>
</Manifest>
```
