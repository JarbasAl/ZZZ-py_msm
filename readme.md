## Py MSM
[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/1QJNhKM8tVv62XSUrST2vnaMXh5ADSyYP8)](https://en.cryptobadges.io/donate/1QJNhKM8tVv62XSUrST2vnaMXh5ADSyYP8)
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/jarbasai)
<span class="badge-patreon"><a href="https://www.patreon.com/jarbasAI" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>
[![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/JarbasAl)

Mycroft Skill Manager, in python!

Development of this repository moved, get the latest version at [MycroftAI/mycroft-skills-manager](https://github.com/MycroftAI/mycroft-skills-manager/)

Archived for Historical reasons only


## install

    pip install py_msm

## Usage

    from py_msm import MycroftSkillsManager

    msm = MycroftSkillsManager()
    
    # msm = MycroftSkillsManager(skills_config={"directory":"some/test/path"})
    
    print msm.platform
    print msm.default_skills
    print msm.installed_skills
    print msm.list_skills()
    print msm.url_info("https://github.com/JarbasAl/skill-stephen-hawking")
    print msm.name_info("date time")
    msm.update_skills()
    msm.remove_by_name("stephen hawking")
    msm.install_by_name("diagnostics")
    msm.install_defaults()
    msm.remove_from_priority_list("skill-pairing")
    msm.add_to_blacklist("skill-pairing")
    msm.reload_skill("skill-pairing")
    
can also be used with [jarbas-skills-repo](https://github.com/JarbasAl/jarbas_skills_repo)

## TODO

- allow passing mycroft root dir in constructor (ensure mycroft is always found for import)
- permissions issues in mark1/picroft - prepare_msm.sh script
- get hashes before git pulling to decide if pip and res.sh should be run
- ensure skill master branch is checked out, else dont update
- use standard msm error codes
- handle pip sudo if not in venv
- requirements.sh guide / template
- standalone command line util
- mycroft skill with stats about skills repo and installed skills
- [auto create readme.md](https://rawgit.com/MycroftAI/mycroft-skills/master/meta_editor.html) for skills
- parse readme.md from skills
- skiller.sh functionality
- submit skill to skills repo
- documentation

## Extras

- checks for skill_requirements.txt, will install skills listed there

## troubleshooting

got problem? most likely you forgot 

    workon mycroft
    
this needs mycroft core installed to run, which in a desktop implies virtual env installation


## Credits

JarbasAI
