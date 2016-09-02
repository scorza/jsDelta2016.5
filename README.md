# jsDelta
GPU implementation of delta mush for Maya 2016.5.

A few changes in the GPU override class, so I'm keeping 2016.5 in a different repo for now.

The file jsDelta.cl MUST be in the same folder alongside the compiled plugin for GPU override to work.

Loading plugin adds command "jsDeltaCmd()" to maya.cmds. Select target mesh and run command from the script editor. You can also create a bare node with deformer(type="jsDelta").

2016.5 Changes:
- getOpenCLCommandQueue has been replaced with getMayaDefaultOpenCLCommandQueue
- MGPUDeformerRegistrationInfo class now requires two separate validation functions instead of validateNode()
- the 2016.5 validate functions (mentioned I think in the 2016 docs but I never implemented them) are validateNodeValues() and validateNodeInGraph()
