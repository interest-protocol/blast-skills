# Blast Skills

Agent skills for launching coins on Blast and contributing to its SDK and
smart contracts.

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

## Blast Contribute

Find an actionable GitHub issue in the Blast TypeScript SDK or Sui Move
contracts, implement and verify a focused fix, and prepare a pull request.
Read the [contribution skill](skills/blast-contribute/SKILL.md) for the full
workflow.

Install with the skills CLI.

```sh
npx skills add interest-protocol/blast-skills --skill blast-contribute
```

Then ask your assistant to find an issue or give it an issue URL.

```text
Use Blast Contribute to find an actionable SDK or contracts issue, fix it,
run the relevant checks, and open a draft PR.
```

## Maintain the skills

Edit the relevant `SKILL.md` and any affected linked references together.
For launch guidance, keep contract behavior, deployment availability,
precedents and planning assumptions distinct. Keep private launch inputs
and generated client plans outside this repository.
