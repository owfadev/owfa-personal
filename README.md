# owfa-personal

**OWFA personal suite** — the default information-organization package: the 21 former core plugins (calendar, cron, device, domain, hot, index, instance-git, language, link, log, mapping, notes, sessions, structure, tag, tmp, todo, trust, user-profile, vault, wiki) that give an OWFA instance its wiki container, notes/sessions native zones, vault proxy layer, derived projections (index/tags/hot/log) and the personal time/task territories. Since framework v0.4 these ship as an independent package instead of riding in `.owfa/plugins/core/`; `owfa init` installs it by default, so a fresh instance starts with the full personal information-organization baseline. The package carries no connectors — everything runs on the framework kernel ([owfa](https://github.com/owfadev/owfa)), which owns the plugin mechanics (manifests, projections, lifecycle); see [PKG.yaml](PKG.yaml) for members/compat and the framework's packages doc for the mechanism.

## Machinery

`pipeline.py` lives at the package root (since 0.1.1): the derived-layer post-write pipeline (index / tags / hot / log / verify) is suite machinery — the kernel never calls it. Instance path: `.owfa/plugins/domains/personal/pipeline.py`; the framework tree keeps a deprecated host copy until 0.5.0.
