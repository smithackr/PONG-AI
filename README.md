# README

# PONG-AI

Developed A pong Clone and bot using NEAT algorithm that is nearly
Impossible to beat..!!
<div style="text-align:center;">
    
 ![Demo](/Docs/pong.gif.gif)
 
</div>



How to Install:

1. Clone the Repository to your local Machine using:
    
    <aside>
    🔗 (https://github.com/smithackr/PONG-AI.git)
    
    </aside>
    
2. To train the model following changes need to be made:
    1. Removing the Comment :
        
        ```python
        if __name__ == "__main__":
            local_dir = os.path.dirname(__file__)
            config_path = os.path.join(local_dir, "config.txt")
        
            config = neat.Config(neat.DefaultGenome, neat.DefaultReproduction,
                                 neat.DefaultSpeciesSet, neat.DefaultStagnation,
                                 config_path)
            run_neat(config) ## Remove the comment at line(140).
            test_ai(config)  ## comment out this line. 
        ```
        
        ```python
         111   p = neat.Checkpointer.restore_checkpoint('neat-checkpoint-23')
               #(Comment this line as it stores the last checkpoint to which the model was trained).
         112   p = neat.Population(config)
        
        ```
        
3. All done, Now just run the program to desired checkpoint which can be change by:
    
    ```python
    winner = p.run(eval_genomes, 20) # changing the value
    ```
    

To test the model just revert back the changes that were made to train the model and change the checkpoint to desired number for testing..!!

# ENJOY!!
