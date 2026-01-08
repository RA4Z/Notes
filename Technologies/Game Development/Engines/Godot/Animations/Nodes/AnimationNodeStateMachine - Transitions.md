There are 3 types of transitions:
- _Immediate_: Will switch to the next state immediately.
- _Sync_: Will switch to the next state immediately, but will seek the new state to the playback position of the old state.
- _At End_: Will wait for the current state playback to end, then switch to the beginning of the next state animation.

Transitions also have a few properties. Click a transition and it will be displayed in the inspector:
![[StateMachine Transitions.png]]

- _Xfade Time_ is the time to cross-fade between this state and the next.
- _Xfade Curve_ is a cross-fade following a curve rather than a linear blend.
- _Reset_ determines whether the state you are switching into plays from the beginning (true) or not (false).
- _Priority_ is used together with the `travel()` function from code (more on this later). Lower priority transitions are preferred when travelling through the tree.
- _Switch Mode_ is the transition type (see above). It can be changed after creation here.
- _Advance Mode_ determines the advance mode. If `Disabled`, the transition will not be used. If `Enabled`, the transition will only be used during `travel()`. If `Auto`, the transition will be used if the advance condition and expression are true, or if there are no advance conditions/expressions.

The last 2 properties in a StateMachine transition are `Advance Condition` and `Advance Expression.` When the Advance Mode is set to _Auto_, these determine if the transition will advance or not.

Advance Condition is a true/false check. You may put a custom variable name in the text field, and when the StateMachine reaches this transition, it will check if your variable is _true_. If so, the transition continues. Note that the advance condition **only** checks if a variable is _true_, and it cannot check for falseness.

This gives the Advance Condition a very limited capability. If you wanted to make a transition back and forth based on one property, you would need to make 2 variables that have opposite values, and check if either of them are true. This is why, in Godot 4, the Advance Expression was added.

The Advance Expression works similar to the Advance Condition, but instead of checking if one variable is true, it evaluates any expression. An expression is anything you could put in an `if` statement. These are all examples of expressions that would work in the Advance Expression:

- `is_walking`
- `is_walking` == true
- `is_walking && !is_idle`
- `velocity > 0`
- `player.is_on_floor()`

Here is an example of an improperly-set-up StateMachine transition using Advance Condition:
![[animtree_badanimcondition.webp]]
![[animtree_badanimcondition.gif]]

This is not working because there is a `!` variable in the Advance Condition, which cannot be checked.

Here is the same example, set up properly, using two opposite variables
![[animtree_goodanimcondition.webp]]
![[animtree_goodanimcondition 1.webp]]

Here is the same example, but using Advance Expression rather than Advance Condition, which eliminates the need for two variables:
![[animtree_goodanimexpression.webp]]
![[animtree_goodanimexpression2.webp]]
![[animtree_goodanimexpression.gif]]
In order to use Advance Expressions, the Advance Expression Base Node has to be set from the Inspector of the [[AnimationTree]] node. By default, it is set to the [[AnimationTree]] node itself, but it needs to point to whatever node contains the script with your animation variables