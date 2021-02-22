# ExTraMapper
ExTraMapper is a tool to find Exon and Transcript-level Mappings of a given pair of orthologous genes between two organisms using sequence conservation. The figure below shows the overall schematic description of ExTraMapper mapping the homologous transcript and exon-pairs between human and mouse genome. 


![ExTraMapper_Figure](https://user-images.githubusercontent.com/18036388/90572310-8b693e00-e168-11ea-9fbc-8188c2834de9.jpg)

# Steps to run ExtraMapper (For python version 3 or later usage)
### Step 1: Prepare the input files
ExTraMapper requires a set of preprocessed files to find the conservation scores. Examples to create these files are provided within __Human-Mouse-Preprocess-Data__ and __Human-Mokey-Preprocessed-Data__ folders. Users should look into these folders and follow the instructions to create the required input files before going to the next step.   


### Step 2: Set the following path
export EXTRAMAPPER_DIR=/path/to/this/folder

### Set the liftover minimum match threshold
MAPPED_EXON_THRES=1.0

### An example input gene pair (BRAF)
genePairId="ENSG00000157764-ENSMUSG00000002413"

### Run ExTramapper (Requires python 2.7)
python $EXTRAMAPPER_DIR/scripts/ExTraMapper.py $MAPPED_EXON_THRES $org1 $org2 $genePairId > Outputs.txt

### Check the run-ExTraMapper.sh for more details
