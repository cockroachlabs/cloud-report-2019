# cloud-report-2019

Details about and from the Cloud Report done in Q3 2019

In 2018, we produced a "Cloud Report", wherein we assessed the performance of AWS vs. GCP along dimensions like TPC-C throughput, I/O, CPU and latency. This year, we aim to produce a similar report but including Azure.

This repo will let us aggregate and share data among team members, including processes and results. 

[Project plan doc](https://docs.google.com/document/d/195l-Opbq_Pd3hHqRM5ynUa4FOtyGJqCriUYfqji38VI/edit)

## Results

You can view the raw results of these tests in the `results` directory of this repo, or in [a spreadsheet where results are automatically tracked](https://docs.google.com/spreadsheets/d/175Q3g3Ti40rEmaCMwm0CBXRnHIo07WSBsxOVhmqNyEY).

## Enclosed Binary

The go program contained in this repo can automatically run tests on cloud providers baked into Roachprod, as well as Microsoft Azure.

For more details, see `reproduction-steps.md` in this repo.

_Note_: It would be possible to extend this binary to run on other platforms relatively easily, but requires some work to handle cloud-specific tasks––namely, getting machine metadata.

## Future Work

When Azure is baked into `roachprod`, one might be able to simply add `azure` to `cloudDetails/default.json` and things will work. At that point you could remove all of the Azure machinery. However, I think that leaving in the `shellRunner` might be nice because it would let us extend this kind of framework into something more like an arbitrary script runner.

## Staff

**Andy Woods** for Product
- Vision, structure, messaging, writing

**Jessica Edwards** for Marketing
- Report production and promotion, messaging

**Jim Walker** for Product Marketing
- Messaging, direction, and competitive landscape

**Nathan VanBenschoten** for Engineering
- Technical oversight and insight

**Sean Loiselle** for Product Marketing
- Data collection and aggregation
