# Example: E-commerce Checkout Discovery

This is a complete walkthrough of using the Cagan framework for a real scenario.

---

## Scenario

A product team at an e-commerce company wants to improve mobile checkout. The PM has a hypothesis that checkout is too slow, but hasn't validated it with customers yet.

---

## Stage 1: Problem Validation

### Team Inputs

**Problem Hypothesis:** Mobile checkout is slow, causing cart abandonment

**North Star:** Increase mobile conversion rate from 1.2% to 3% within 6 months

**Preliminary Evidence:**
- Support tickets mention slowness
- User testing observations show hesitation
- ~30% of abandoners cite other reasons (shipping cost, lack of saved cards)

### What Gets Generated

**File:** `/project/discovery/01-problem-validation.md`

Risk Assessment:
- Value Risk: MEDIUM-HIGH (some evidence, but contradictory)
- Usability Risk: MEDIUM (unknown if design is the problem)
- Viability Risk: LOW (fits strategy, revenue-bearing)
- Feasibility Risk: LOW (no unknown technical challenges)

**Decision:** GO - Proceed to discovery

---

## Stage 2: Discovery Planning

### Team Inputs

**Timeline:** 3 weeks for discovery

**Target Segments:**
- Mobile-first users
- Repeat customers  
- Recent abandoners

**Team:** PM (Jane) + Designer (Mike) + Engineer (Alex)

### What Gets Generated

**Files:**
- `/project/discovery/02-discovery-plan.md`
- `/project/discovery/03-interview-guide.md`

**Discovery Plan includes:**
- Research objectives (tied to value/usability risks)
- Recruiting strategy (20 customers: 8 abandoners, 7 recent completers, 5 power users)
- Timeline (3 weeks, staggered interviews)
- Team roles (PM leads, Designer observes UX, Engineer notes technical blockers)

**Interview Guide includes:**
- Screener to confirm right participant
- Core questions: "Walk me through your last checkout attempt"
- Probes about current solution and workarounds
- Explicit instruction: Don't mention solution, focus on problem discovery

---

## Stage 3: Discovery Execution

### What Team Does (2 weeks)

- Conduct 20 customer interviews (30-45 min each)
- PM, Designer, Engineer attend interviews together
- Real-time note-taking using template
- Tag observations: speed issues, trust concerns, form friction, confusion

### Key Behaviors

PM asks: "Walk me through your last attempt to buy on mobile"

Customer shares: Took 3.5 minutes, had to re-enter address, worried about credit card security, almost abandoned before hitting "confirm"

Designer notes: User hesitated at payment page, re-read security text
Engineer notes: Address field required specific format, took multiple attempts

---

## Stage 4: Discovery Synthesis

### Team Workshop (1 week)

Team watches all 20 interviews together.

Creates affinity map:

**Theme A: Speed Concerns** (8 customers)
- Common: Slow 3G networks, checkout took >2 min
- Jobs to be done: "Get through checkout quickly"

**Theme B: Trust/Security** (7 customers)
- Common: Worried about entering payment info, no trust signals visible
- Jobs to be done: "Complete checkout feeling secure"

**Theme C: Form Friction** (6 customers)
- Common: Address entry tedious on small keyboard, postal code formats confusing
- Jobs to be done: "Enter information easily on mobile"

**Theme D: Progress Clarity** (5 customers)
- Common: Don't know how many steps remain, felt trapped
- Jobs to be done: "Know checkout progress clearly"

### Key Contradiction

Some customers said "speed is most important," but interviews revealed they were equally concerned about trust. When Mike showed them a fast checkout UI without security signals, they weren't interested. When he showed a slower checkout with clear security indicators, they engaged.

### Output

**File:** `/project/discovery/03-discovery-readout.md`

**Key Findings:**
1. Speed is A problem, not THE problem (8/20 vs. 7/20 on trust)
2. Trust is underestimated barrier (security signals matter more than stated)
3. Form friction is solvable bottleneck (address autofill would help 6/20)
4. Progress clarity affects engagement (5/20 want to know steps)
5. Behavior contradicts stated preferences (see contradiction above)

---

## Stage 5: Strategy Definition

### Team Review

**Has the problem changed?** Yes. Originally thought speed alone was the issue. Now know it's speed + trust + friction.

**Do we still want to solve this?** Yes, but with broader scope.

**Strategic priority?** Yes, high-impact opportunity.

### What Gets Generated

**File:** `/project/strategy/01-okr-definition.md`

```
Objective: Increase mobile conversion rate from 1.2% to 3%

Key Results:
1. Reduce avg checkout time from 3m 20s to 2m 30s
   - Metric: Average checkout duration
   - Target: 2m 30s
   - Measurement: Analytics event timing

2. Increase trust perception from 6.2 to 8.0
   - Metric: Post-checkout survey (security perception)
   - Target: 8.0/10
   - Measurement: In-product survey

3. Reduce form abandonment from 12% to <5%
   - Metric: % abandonment at form-entry step
   - Target: <5%
   - Measurement: Analytics

4. Increase repeat purchase rate (mobile) from 18% to 25%
   - Metric: Mobile repeat customer %
   - Target: 25%
   - Measurement: Cohort analysis
```

**File:** `/project/strategy/02-strategic-bet.md`

```
Bet Statement: If we address speed, trust signals, and form friction together, 
mobile checkout conversion will increase to 3%, driving $2M+ in incremental revenue

Why This Bet:
- Discovery revealed three separate barriers
- Customer segments vary in which matters most (not monolithic problem)
- No single solution; needs multi-pronged approach

Success Looks Like:
- Conversion reaches 2.8%+ within 90 days
- Form drop-off decreases significantly  
- Trust perception increases
- Repeat purchase rate increases

Key Assumptions:
1. Speed optimization will reduce friction (test: measure before/after)
2. Trust design changes will increase confidence (test: survey + behavior)
3. Form simplification won't reduce data captured (test: compare required vs. optional fields)

Risks:
- Speed alone won't move conversion (customer trust is equally important)
- Form simplification may reduce future order data (tradeoff needed)
- Trust signals are psychological; design changes may have limited impact

Pivots if Wrong:
- If speed optimization doesn't move conversion: Focus on trust design
- If trust design has no impact: Explore alternative trust models (reviews, guarantees)
- If form simplification reduces fulfillment data: Add optional fields later in process

Timeline to Decision: 90 days post-launch
```

**File:** `/project/strategy/03-discovery-to-delivery-handoff.md`

```
What We Discovered:
- Three separate barriers to mobile checkout: speed, trust, form friction
- Customer behaviors contradict stated preferences (say speed, but show concern about trust)
- No single solution; multi-pronged approach needed

What We're Solving:
- Make mobile checkout fast, trustworthy, and frictionless

Who We're Solving For:
- Mobile-first users (primary shoppers)
- Repeat customers (high value)
- Speed-sensitive users (online shoppers, mobile-native cohort)

Key Assumptions to Validate in Build:
- Speed optimization achieves target (test in beta)
- Trust signals are effective (A/B test design options)
- Form simplification doesn't lose needed data (track required vs. optional)

How We'll Measure Impact:
- Post-launch: Daily conversion tracking
- Week 2: Survey trust perception
- Week 4: Analyze form completion patterns
- Week 8: Review repeat purchase rate
```

---

## Results (Hypothetical)

### After 90 Days

**Actual Results:**
- Mobile checkout time: 2m 45s (target: 2m 30s)
- Trust perception: 7.8/10 (target: 8.0/10)
- Form abandonment: 6% (target: <5%)
- Mobile conversion: 2.2% (target: 2.8%+)

**Analysis:**
- Made progress on all metrics, but didn't hit conversion target
- Trust design had bigger impact than speed optimization
- Form simplification was successful
- Repeat purchase rate up 4% (good indicator of longer-term value)

**Next Bet:**
Double down on trust: customer reviews, guarantee badges, payment option expansion

---

## Lessons from This Example

1. **Collaboration matters** - Designer and engineer insights changed the team's understanding
2. **Contradictions are insights** - Stated preference ≠ revealed preference
3. **One solution isn't enough** - Multiple barriers require multiple solutions
4. **Speed to decision** - Full cycle (validation + planning + execution + synthesis + strategy) = 6 weeks
5. **Data informs pivots** - When first bet doesn't fully work, you know why and what to try next
