When you make an `AnimationNodeStateMachine`, you get an empty 2d graph in the bottom panel, under the [[AnimationTree]] tab. It contains a `Start` and `End` state by default.

![[AnimationNodeStateMachine - Image1.png]]

To add states, right click or use the **create new nodes** button, whose icon is a plus in a box. You can add animations, blendspaces, blendtrees, or even another StateMachine. To edit one of these more complex sub-nodes, click on the pencil icon on the right of the state. TO return to the original StateMachine, click **Root** on the top left of the panel.

Before the StateMachine can do anything useful, the states must be connected with transitions. To add a transition, click the **connect nodes** button, which is a line with a right-facing arrow, and drag between two states. You can create 2 transitions between states, one going in each direction.
![[animtree_connections.gif]]
There are different types of [[AnimationNodeStateMachine - Transitions|transitions]] in [[AnimationNodeStateMachine]]


