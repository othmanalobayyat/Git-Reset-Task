---


---

<h1 id="learning-about-the-git-resetsoft-mixed-and-hard">Learning about the <code>'git reset'</code>:Soft, Mixed and Hard</h1>
<p>The <code>git reset</code> command is a powerful tool for undoing changes and moving the HEAD pointer to a previous commit. It operates in three methods <strong>(soft, mixed, and hard)</strong>. Depending on the method used the git rest affects <em>your working area, staging area, and commit history</em>.</p>
<h2 id="git-reset---soft">1. <code>git reset --soft</code></h2>
<p><strong>What it does:</strong> Moves the <code>HEAD</code> pointer to the specified commit and <strong>keeps</strong> all changes in the staging area and working directory, the changes remain staged, but the commit history is reverted.</p>
<p><strong>Usage:</strong> When you want to regroup, add more changes or undo the last commit before recommitting the change again.</p>
<ul>
<li><strong>Example:</strong></li>
</ul>
<pre><code>git reset --soft &lt;commit&gt;
</code></pre>
<h2 id="git-reset---mixed">2. <code>git reset --mixed</code></h2>
<p><strong>What it does:</strong> it’s the <strong>default</strong> behaviour of <code>git reset</code>, it moves the <code>HEAD</code> pointer to the specified commit, <strong>unstages</strong> the changes, but <strong>keeps</strong> them in the working directory, changes remain in the working directory, but you’ll need to stage them again before committing.</p>
<p><strong>Usage:</strong> When you want to undo the last commit and also unstage the changes, so you can modify them before staging and committing again.</p>
<ul>
<li><strong>Example:</strong></li>
</ul>
<pre><code>git reset --mixed &lt;commit&gt;
</code></pre>
<h2 id="git-reset---hard">3. <code>git reset --hard</code></h2>
<p><strong>What it does:</strong> Moves the <code>HEAD</code> pointer to the specified commit and <strong>removes</strong> all changes from both the staging area and working directory, this command will delete all changes for ever.</p>
<p><strong>Usage:</strong> When you want to completely undo all changes, both staged and unstaged, and return to a clean working directory as if the changes were never made.</p>
<ul>
<li><strong>Example:</strong></li>
</ul>
<pre><code>git reset --hard &lt;commit&gt;
</code></pre>
<h2 id="summary">Summary</h2>
<ul>
<li><strong>Soft Reset</strong>: Moves commits back to the staging area, allowing you to regroup or add more changes before recommitting.</li>
<li><strong>Mixed Reset (default)</strong>: Moves commits back to the working directory, making the changes unstaged.</li>
<li><strong>Hard Reset</strong>: Discards commits and their changes completely.</li>
</ul>
<blockquote>
<p><strong>Hint:</strong> You may need to use <code>git log</code> command to get the <strong>commit hash</strong> for the desiring commit.</p>
</blockquote>
<blockquote>
<p>By: Othman Al-Obayyat.</p>
</blockquote>

