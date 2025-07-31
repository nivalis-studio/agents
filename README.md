# agents

Claude code agents used @nivalis-studio

## orchestrators/ - Setup a project or dispatch work

- Team configurator / Staff manager: use on new project, defines which subagents are useful and help split the work. Can ask the code archaeologist for help.
- Task planning subagent / Product manager: MUST be used on every request. Should understand the request and evaluate the next steps. Then it should alwasy call the tech lead subagent.
- CTO: MUST be used on every request. Should dispatch the work between subagents.

## tech-leads/ (can be called by CTO)

- Backend Lead
- Frontend Lead
- Mobile Lead

## devs/ (can be called by a tech lead)

- Algorithm expert
- Nextjs expert
- Rust expert
- Typescript expert
- Go expert
- Expo expert
- Tailwindcss expert

## maintainers/ Code base maintenance (can be called by CTO or a tech lead)

- Code archaeologist: Help understand complex codebases.
- Code tester: Creates and runs tests.
- Code reviwer: Senior Engineer evaluating code cleanness and good practices.
- Code fixer: linter and formatter. Should be a pro in eslint and in @nivalis/eslint-config and prettier rules.
