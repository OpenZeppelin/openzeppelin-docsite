---
id: version-2.1.1-crowdsale_distribution_RefundableCrowdsale
title: RefundableCrowdsale
original_id: crowdsale_distribution_RefundableCrowdsale
---

<div class="contract-doc"><div class="contract"><h2 class="contract-header"><span class="contract-kind">contract</span> RefundableCrowdsale</h2><p class="base-contracts"><span>is</span> <a href="crowdsale_distribution_FinalizableCrowdsale.html">FinalizableCrowdsale</a></p><p class="description">Extension of Crowdsale contract that adds a funding goal, and the possibility of users getting a refund if goal is not met. * Deprecated, use RefundablePostDeliveryCrowdsale instead. Note that if you allow tokens to be traded before the goal is met, then an attack is possible in which the attacker purchases tokens from the crowdsale and when they sees that the goal is unlikely to be met, they sell their tokens (possibly at a discount). The attacker will be refunded when the crowdsale is finalized, and the users that purchased from them will be left with worthless tokens.</p><div class="source">Source: <a href="https://github.com/OpenZeppelin/zeppelin-solidity/blob/v2.1.1/contracts/crowdsale/distribution/RefundableCrowdsale.sol" target="_blank">crowdsale/distribution/RefundableCrowdsale.sol</a></div></div><div class="index"><h2>Index</h2><ul><li><a href="crowdsale_distribution_RefundableCrowdsale.html#_finalization">_finalization</a></li><li><a href="crowdsale_distribution_RefundableCrowdsale.html#_forwardFunds">_forwardFunds</a></li><li><a href="crowdsale_distribution_RefundableCrowdsale.html#claimRefund">claimRefund</a></li><li><a href="crowdsale_distribution_RefundableCrowdsale.html#">fallback</a></li><li><a href="crowdsale_distribution_RefundableCrowdsale.html#goal">goal</a></li><li><a href="crowdsale_distribution_RefundableCrowdsale.html#goalReached">goalReached</a></li></ul></div><div class="reference"><h2>Reference</h2><div class="functions"><h3>Functions</h3><ul><li><div class="item function"><span id="_finalization" class="anchor-marker"></span><h4 class="name">_finalization</h4><div class="body"><code class="signature">function <strong>_finalization</strong><span>() </span><span>internal </span></code><hr/><div class="description"><p>Escrow finalization task, called when finalize() is called.</p></div></div></div></li><li><div class="item function"><span id="_forwardFunds" class="anchor-marker"></span><h4 class="name">_forwardFunds</h4><div class="body"><code class="signature">function <strong>_forwardFunds</strong><span>() </span><span>internal </span></code><hr/><div class="description"><p>Overrides Crowdsale fund forwarding, sending funds to escrow.</p></div></div></div></li><li><div class="item function"><span id="claimRefund" class="anchor-marker"></span><h4 class="name">claimRefund</h4><div class="body"><code class="signature">function <strong>claimRefund</strong><span>(address refundee) </span><span>public </span></code><hr/><div class="description"><p>Investors can claim refunds here if crowdsale is unsuccessful.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>refundee</code> - Whose refund will be claimed.</div></dd></dl></div></div></li><li><div class="item function"><span id="fallback" class="anchor-marker"></span><h4 class="name">fallback</h4><div class="body"><code class="signature">function <strong></strong><span>(uint256 goal) </span><span>public </span></code><hr/><div class="description"><p>Constructor, creates RefundEscrow.</p></div><dl><dt><span class="label-parameters">Parameters:</span></dt><dd><div><code>goal</code> - Funding goal</div></dd></dl></div></div></li><li><div class="item function"><span id="goal" class="anchor-marker"></span><h4 class="name">goal</h4><div class="body"><code class="signature">function <strong>goal</strong><span>() </span><span>public </span><span>view </span><span>returns  (uint256) </span></code><hr/><dl><dt><span class="label-return">Returns:</span></dt><dd>minimum amount of funds to be raised in wei.</dd></dl></div></div></li><li><div class="item function"><span id="goalReached" class="anchor-marker"></span><h4 class="name">goalReached</h4><div class="body"><code class="signature">function <strong>goalReached</strong><span>() </span><span>public </span><span>view </span><span>returns  (bool) </span></code><hr/><div class="description"><p>Checks whether funding goal was reached.</p></div><dl><dt><span class="label-return">Returns:</span></dt><dd>Whether funding goal was reached</dd></dl></div></div></li></ul></div></div></div>