# ModLinks

This is the repository that holds information on every public mod that should be accessible via mod installers.

## How to add/update a mod to ModLinks

1. don't create a fork
1. go to https://github.com/hk-modding/modlinks/blob/main/ModLinks.xml
1. click the pencil at the top right corner
1. make the changes
1. scroll to the bottom of the github page and click the button that says propose changes
1. do that and it should also give an option to delete that branch after the pull request got merged.

## Example manifest

```xml
<Manifest>
    <Name>Test Name</Name>
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
    <Integrations>
        <Integration>Another mod's name, like the dependency list, but not a hard dependency, but extra stuff when it is installed alongside</Integration>
    </Integrations>
    <Tags>
        <Tag>Either of: 'Boss', 'Cosmetic', 'Expansion', 'Gameplay', 'Library', 'Utility'</Tag>
    </Tags>
    <Authors>
        <Author>An author's name. Has no specific format.</Author>
    </Authors>
    <Issues>
        <![CDATA[https://website/for/bug_reports]]>
    </Issues>
</Manifest>
```
