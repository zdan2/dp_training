ステップ1: 「配るDP」と「貰うDP」の基本を徹底する
まずは1次元DPと、基本的なナップサック問題です。状態をどう定義するか、遷移をどう書くかに慣れます。
[AtCoder]
A - Frog 1
B - Frog 2
C - Vacation
D - Knapsack 1
E - Knapsack 2 (「何をDPの添字にするか」を考える良問)
[LeetCode]
70. Climbing Stairs: Frog 1とほぼ同じ問題。DPの第一歩です。
198. House Robber: Vacation (C) と類似の「隣接するものは選べない」パターンの基本形です。
300. Longest Increasing Subsequence (LIS): 最長増加部分列。$O(N^2)$ のDP解法をまずマスターしましょう（$O(N \log N)$解法はDPとは別のアプローチです）。
416. Partition Equal Subset Sum: Knapsack 1 (D) の亜種。「合計値の半分をピッタリ作れるか」という問題に帰着させます。
322. Coin Change: 「個数制限なしナップサック」（完全ナップサック）の典型問題です。

ステップ2: 典型パターンの習得 (1) - 区間DP & ビットDP
線形DP以外の主要なパターンを学びます。
[AtCoder]
N - Slimes (区間DP)
O - Matching (ビットDP)
[LeetCode]
516. Longest Palindromic Subsequence: 最長回文「部分列」。dp[i][j] を「区間 $i$ から $j$ における答え」とする典型的な区間DPです。
698. Partition to K Equal Sum Subsets: ビットDP（または状態圧縮DP）の練習になります。「どの数字をすでに使ったか」をビットマスクで管理します。

ステップ3: 典型パターンの習得 (2) - 経路DP & 文字列DP
応用範囲の広い2つのパターンと、DPの「復元」を学びます。
[AtCoder]
H - Grid 1 (経路DP)
F - LCS (文字列DP + 復元)
G - Longest Path (DAG上のDP)
[LeetCode]
62. Unique Paths: Grid 1 (H) と全く同じ、グリッド上の経路数え上げです。
64. Minimum Path Sum: 経路DPで「最小コスト」を求めるパターンです。
1143. Longest Common Subsequence: LCS (F) と全く同じ、文字列DPの基本です。
72. Edit Distance: 編集距離。LCSと並ぶ、文字列DPの超典型問題です。
123. Best Time to Buy and Sell Stock III: 「状態」をより複雑に持つDPの練習。「$k$回取引した」「株を持っている/持っていない」などを状態に加えます（状態マシンDP）。

ステップ4: 中級への扉 - 確率DP & 期待値DP
DPで確率や期待値を扱う、中級者への登竜門です。
[AtCoder]
I - Coins (確率DP)
J - Sushi (期待値DP)
[LeetCode]
688. Knight Probability in Chessboard: 確率DPの良問です。$K$回の移動後、ナイトが盤上にいる確率を計算します。
837. New 21 Game: 期待値・確率DPの良問。遷移が少し複雑で考えさせられます。

ステップ5: さらなる発展 - 木DP & 桁DP
これらが解ければ、もう初級者ではありません。
[AtCoder]
P - Independent Set (木DP)
S - Digit Sum (桁DP)
M - Candies (累積和によるDP高速化)
[LeetCode]
337. House Robber III: House Robber (198) の木バージョン。典型的な木DPです。
600. Non-negative Integers without Consecutive Ones: 典型的な桁DP。「$N$以下で、2進数表現で1が連続しないものの個数」を求めます。
139. Word Break: dp[i] を「文字列の先頭 $i$ 文字が辞書の単語で区切れるか」と定義する、文字列と辞書を組み合わせたDPです。

学習のヒント (再掲)
図（テーブル）を描く: DPテーブルを紙に書き、遷移を可視化するのが最強のデバッグ方法です。
状態と遷移を言葉にする: 「dp[i]とは何か」「dp[i]をどう計算するか」をコーディングの前に明確にします。
メモ化再帰を併用する: forループのDP（ボトムアップ）が難しく感じる場合は、再帰関数（トップダウン、メモ化再帰）で考えると、状態遷移が直感的になることがあります。
解説を賢く使う: 30分～1時間考えて分からなければ解説を読みます。ただし、解法（状態と遷移の設計）を理解したら、必ず自力で実装してください。
反復練習: 一度解けた問題も、1週間後に何も見ずに解けるか試すことで、パターンが定着します。
