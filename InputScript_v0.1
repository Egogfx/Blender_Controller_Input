#https://github.com/dfelinto/blender/blob/master/release/scripts/templates_py/operator_modal_timer.py

#FIGURE OUT HOW TO SELECT THE REMOTE CONTROLLED COLLECTION AUTOMATICALLY.

import bpy
import XInput   #The Module that lets me access the controller. Although it's looking for Xbox controller. Which is why we use Dualsense X. 

#bpy.ops.screen.animation_play() #Plays the timeline to record keyframes

#/////////////////////////////////////

class ModalTimerOperator(bpy.types.Operator):
    """Operator which runs itself from a timer"""
    bl_idname = "wm.modal_timer_operator"
    bl_label = "Modal Timer Operator"

    _timer = None

    def modal(self, context, event):
        if event.type in {'RIGHTMOUSE', 'ESC', 'LEFTMOUSE'}:
            bpy.ops.screen.animation_cancel()
# Resets the timeline before cancelling the program.
            self.cancel(context)
            
            return {'CANCELLED'}
        


        #Controller Code
        #!!SOFTWARE DUALSENSE X must be running for PS5 controller to be recognized in Xinput
        if event.type == 'TIMER':
            state=XInput.get_state(0)
            
            R1 = XInput.get_button_values(state)['RIGHT_SHOULDER']
            
# Setting variables for easier reading.       
            
            LeftThumbX = XInput.get_thumb_values(state)[0][0]
            LeftThumbY = XInput.get_thumb_values(state)[0][1]
            RightThumbX = XInput.get_thumb_values(state)[1][0]*1
            RightThumbY = XInput.get_thumb_values(state)[1][1]*-1
            
            L3 = XInput.get_button_values(state)['LEFT_THUMB']
            R3 = XInput.get_button_values(state)['RIGHT_THUMB']
            
            RightTrigger = XInput.get_trigger_values(state)[1]
            LeftTrigger = XInput.get_trigger_values(state)[0]
            
            LeftShoulder = XInput.get_button_values(state)['LEFT_SHOULDER']
            RightShoulder = XInput.get_button_values(state)['RIGHT_SHOULDER']
            
            DPadUP = XInput.get_button_values(state)['DPAD_UP']
            DPadDOWN = XInput.get_button_values(state)['DPAD_DOWN']
            DPadLEFT = XInput.get_button_values(state)['DPAD_LEFT']
            DPadRight = XInput.get_button_values(state)['DPAD_RIGHT']
            
            START = XInput.get_button_values(state)['START']
            BACK = XInput.get_button_values(state)['BACK']
            
            A = XInput.get_button_values(state)['A']
            B = XInput.get_button_values(state)['B']
            X = XInput.get_button_values(state)['X']
            Y = XInput.get_button_values(state)['Y']
            
#//////////////////// </Variables> \\\\\\\\\\\\\\\\\\\\\\\\\\\\   


            if BACK:                        #Pressing Back to end the script.
                bpy.ops.screen.animation_cancel()   #Resets the timeline before cancelling the program.
                self.cancel(context)
                print("Back Button Pressed")
                
                return {'CANCELLED'}

#            event = get_events()
  


#Objects to control:
            
        #Head Rotation
#            bpy.data.objects["Head Controller.001"].rotation_euler[0] = RightThumbY

        #Rig Main Bone Movement  
#            bpy.data.objects["Head Controller.001"].location[0] = LeftThumbX/2
#            bpy.data.objects["SkeletalPosition_Empty"].rotation_euler[2] = LeftThumbX
#            print(bpy.data.objects["SkeletalPosition_Empty"].rotation_euler[2])
#            LeftThumbYCorrected = LeftThumbY/1.3
#            print(LeftThumbYCorrected)
#            bpy.data.objects["Head Controller.001"].location[2] = LeftThumbYCorrected+4
            
            #Next line means if RightShoulder is True, rot Y, otherwise rot Z.
#            if R3:
#                bpy.data.objects["Head Controller.001"].rotation_euler[1] = RightThumbX
#            else:
#                bpy.data.objects["Head Controller.001"].rotation_euler[1] = 0 #Resets the Head lean to 0 as soon as L1 is released.
#                bpy.data.objects["Head Controller.001"].rotation_euler[2] = RightThumbX
            
  # The IF Statement above is to Hold R1 to Lean Head sideways, tilt's weird, seems to mix inputs instead.#

            MouthOpen = "Icosphere"
            MouthOpenZ = bpy.data.objects[MouthOpen]
        #Speak
            MouthOpenZ.location[2] = RightTrigger*2
            MouthOpenZ.location[1] = LeftThumbX
#            bpy.data.objects["QBlink.cont"].location[2] = LeftShoulder

        #Expression Shapekeys
#            bpy.data.objects["Smile.Controller"].location[2] = A       #LeftThumbX
#            bpy.data.objects["Frown.cont"].location[2] = X           #LeftThumbX*-1
#            bpy.data.objects["O.cont"].location[2] = B               #LeftThumbY*-1
#            bpy.data.objects["Open.cont"].location[2] = Y           #LeftThumbY
#            bpy.data.objects["anger.cont"].location[2] = LeftTrigger
#            
#      \\\\\\\\\\\\\\\\\\\\\\   < / I N P U T > //////////////////


# This line selects the currently highlighted object ONLY.
#            obj = bpy.context.object
    

# set the keyframe at current frame for all objects selected thanks to the 'for' loop. 
            
            
#            for obj in bpy.context.selected_objects:
#                obj.keyframe_insert(data_path="rotation_euler", frame=bpy.context.scene.frame_current, )    
#                obj.keyframe_insert(data_path="location", frame=bpy.context.scene.frame_current, )         


#////////////////////////////////////////////////////////

          
        return {'PASS_THROUGH'}

    def execute(self, context):
        wm = context.window_manager
    
        time = 0.1
        
        self._timer = wm.event_timer_add(time, window=context.window)
        wm.modal_handler_add(self)
        return {'RUNNING_MODAL'}

    def cancel(self, context):
        wm = context.window_manager
        wm.event_timer_remove(self._timer)


def menu_func(self, context):
    self.layout.operator(ModalTimerOperator.bl_idname, text=ModalTimerOperator.bl_label)


def register():
    bpy.utils.register_class(ModalTimerOperator)
    bpy.types.VIEW3D_MT_view.append(menu_func)

# Register and add to the "view" menu (required to also use F3 search "Modal Timer Operator" for quick access)
def unregister():
    bpy.utils.unregister_class(ModalTimerOperator)
    bpy.types.VIEW3D_MT_view.remove(menu_func)

0
if __name__ == "__main__":
    register()

    # test call
    bpy.ops.wm.modal_timer_operator()
