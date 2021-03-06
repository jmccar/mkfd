# Sample playbook
This sample includes the `mkfd` role for the purposes of providing a complete
example of how the role is meant to be used. The key files to review in this
repository are:
  * `host_vars/localhost.yml`: The variables used by the playbook. Some of
    these are scenario-specific, such as the corporate servers and site subnets.
    Some of them are inputs to the role, such as `doc_name` and `make_zip`.
  * `doc_inputs/SITE.j2`: A mix of Jinja2/LaTeX code, this file describes a
    branch site validation procedure. It includes lists, diagrams, user input
    fields, and some other useful techniques.
  * `config_templates/`: Each branch has one router and one switch, thus there
    are two templates total. The templates are simple and contain only variable
    substitution, which allows junior engineers to maintain them.
  * `infra_templates/`: Since Cisco ISE running TACACS needs to be updated as
    new branches are brought online, a CSV is generated here. It can be
    imported into ISE to save time on infrastructure updates to support the new
    branch sites.
  * `files/`: The unzipped file structure as generated by the tool. Examine
    the branch router/switch configuration files and the per-site documentation
    generated by the role.
  * `archives/`: The exact same data in the `files/` folder, except in archive
    form. You may download this bundle to view/edit the content locally.
