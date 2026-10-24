# Citation grounding auditor

주장의 인용문·문서 버전·행 범위를 확인하고 구조화된 상충 주장을 드러낸다.

A focused executable resource for AI-assisted structured work. **Zero runtime dependencies, no API key, Node.js 22+.**

[Live workspace](https://proofnova.github.io/citation-grounding/) · [한국어 리소스 모음](https://proofnova.github.io/) · [Task contract](resource.json) · [Prior art](RESEARCH.md)

```sh
git clone https://github.com/proofnova/citation-grounding.git
cd citation-grounding
npm test
node cli.mjs example.json
```

## What it does

Exact excerpt location and optional document hash binding without pretending to judge meaning.

A real quote is not automatically semantic support, and a changed source cannot reuse an old digest.

## Connect a model

Import `execute` from `./run.mjs`. Expose this declared tool to your model, validate its tool name/input contract, execute it, and retain the returned JSON and input digest. Calculations and constraint checks are performed by the resource. No paid model or new agent framework is required.

[SKILL.md](SKILL.md) contains the workflow, interpretation and recovery procedure. [example.json](example.json) is a complete input; [cases.json](cases.json) contains worked and edge-case synthetic regression checks. The website executes the same code locally in a bounded Worker. It has no model or external data upload.

## Recovery and limits

Locate the actual source excerpt or repair its range/version; send semantic support questions to domain review.

Underlying algorithms and task outcomes already exist in the alternatives. An existing tool configured for this exact task may remove the need for a separate project. Small synthetic tests cannot establish broad expertise or external demand. See [RESEARCH.md](RESEARCH.md). A plan/audit is not an external action or proof of actual user benefit.

## Contribute

Open an issue with a synthetic/redacted failing JSON input, expected result and Node version. Add a regression test and run `npm test`. Never include credentials or real private records in public examples.

MIT · Proofnova · 2026
