---
layout: post
title: Bad Variable Name
date: '2012-02-05T00:28:09-08:00'
tags: []
tumblr_url: https://fugugames.tumblr.com/post/110515821606/bad-variable-name
---
The latest update of [HyperBowl](http://hyperbowl3d.com/) fixes one of those embarrassing bugs that you can’t believe has been there all this time. It might not have been there from the beginning - in the function below, which calculates the score for a frame that rolled a strike, the parameter was named “frame”, but then I think at some point I got paranoid that I was actually referencing a static variable named “frame” which represents the current frame. But somehow I still used “frame” instead of “f” to check if we’ve reached the ninth frame, and since we may be calculating strike scores two frames behind the current one, I’m really treating the seventh and eighth frames specially, thus depriving players of perfect 300 scores.

This may look like a case of don’t-use-global-variables, but “frame” could easily be non-static and not change the problem. It’s really a case of bad variable naming - we’re not talking Hungarian notation here, just a more precise name like “currentFrame” would have avoided this confusion (and then “frame” would be a much improved parameter name over “f”). So I’ll fix that…yeah, one of these days…

`
// calculate and set the strike score for the given frame
// not called for the final frame
function SetStrikeScore(f:int) {
var scores:FrameScore[] = GetCurrentPlayer().scores;
var framescore:FrameScore = scores[f];
framescore.total = framescore.ball1;
// always add the score from first roll of the next frame
framescore.total+=scores[f+1].ball1;
// if not the ninth or tenth frame, and the next frame is a strike, then add the the ball1 score from the frame after that
if (f < 8 && IsStrike(f+1)) {
framescore.total+=scores[f+2].ball1;
} else {
// for the ninth frame (frame 8) add the second ball from the next (final) frame (there always is one)
framescore.total+=scores[f+1].ball2;
}
}`

