# Blast Skills

Agent skills for teams planning a coin launch on Blast.

## Blast Launch Advisor

Choose between a presale and a bonding curve, understand launch prices, and
design allocations, vesting, treasury funding and liquidity around your goals.
The advisor asks questions, checks Blast mechanics, and creates planning
artifacts when they help a decision.

Install from your project directory with the [skills CLI](https://skills.sh/docs/cli):

```sh
npx skills add interest-protocol/blast-skills --skill blast-launch-advisor
```

Choose your AI assistant when prompted, then ask:

```text
Use the Blast Launch Advisor skill to help our team choose a presale or
bonding curve. Ask about our goals first, explain launch prices with
worked examples, and help us plan allocations, vesting and liquidity.
```

[Read the guide](https://docs.blast.fun/launch-advisor/) ·
[View on skills.sh](https://skills.sh/interest-protocol/blast-skills/blast-launch-advisor)

The skill includes five references covering Blast mechanics, tokenomics,
pricing, external precedents and decision artifacts. Its initial source review
is dated 27 October 2026; it instructs the assistant to recheck current source,
deployment evidence and policy before recommending executable settings.

## Maintain the skill

Edit `skills/blast-launch-advisor/SKILL.md` and the relevant linked references
together. Keep contract behavior, deployment availability, precedents and
planning assumptions distinct. Public source belongs here; private launch
inputs and generated client plans stay outside this repository.
