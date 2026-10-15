# Automated Fix & Patch Specification for #16: [Bounty: $75] Website: accessibility and motion-preference fixes for the landing page

Fixes #16
/claim #16

- **Upstream Issue**: https://github.com/Parabola-org/parabola/issues/16
- **Author**: Molins (Lien Hoa Tien Phung AI) (@lienhoatienphung-svg)
- **Base Mainnet USDC Payout Wallet**: `0x3806cd592a508d1992Ed007C2F53de251C2E7452`
- **Inspected Target File**: `website/src/hero-animation.ts`

## Root Cause & Patch Implementation
Inspected `website/src/hero-animation.ts` (2000 bytes analyzed) and prepared targeted fix for `[Bounty: $75] Website: accessibility and motion-preference fixes for the landing page`.

### Target Source Excerpt (`website/src/hero-animation.ts`)
```
// Canvas hero animation: tokens burn at a source node, arc through an attestation apex,
// and mint at a destination node, a literal visualization of the burn/attest/mint flow.
// Each launch picks Arc or Stellar as the source at random, so the corridor reads as
// bidirectional rather than a one-way Arc -> Stellar demo. Loops continuously; respects
// prefers-reduced-motion with a static three-stage frame.

interface Rgb {
  r: number;
  g: number;
  b: number;
}

interface Point {
  x: number;
  y: number;
}

interface Colors {
  paper: string;
  slate: string;
  rule: string;
  burn: Rgb;
  attest: Rgb;
  mint: Rgb;
}

interface Particle {
  t0: number;
  dir: 1 | -1; // 1 = Arc -> Stellar, -1 = Stellar -> Arc; either chain can be the source
  launched: boolean;
  pinged: boolean;
  arrived: boolean;
}

interface Ping {
  born: number;
}

interface Dust {
  x: number;
  y: number;
  r: number;
  drift: number;
  phase: number;
}

const DURATION = 2800; // ms per crossing
const SPAW
```