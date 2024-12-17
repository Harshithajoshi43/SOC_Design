# Digital VLSI SoC_design and planning
## Day 1

<details>
  <summary>Lab</summary>
 
1. Run 'picorv32a' design synthesis using OpenLANE flow and generate necessary outputs.
Screenshots of running each commands

```
cd Desktop/work/tools/openlane_working_dir/openlane
```

```
docker
```

```
./flow.tcl -interactive
```

```
package require openlane 0.9

```

```
prep -design picorv32a
```


![Screenshot 2024-11-28 010505](https://github.com/user-attachments/assets/9b9ebfb9-2997-45c7-96e5-f8895d4e7b89)


```
run_synthesis
```
![Screenshot 2024-11-28 010750](https://github.com/user-attachments/assets/c0bc9a60-38ff-4ccf-9a24-458875dd37ef)
2. Calculate the flop ratio.
![Screenshot 2024-11-28 010807](https://github.com/user-attachments/assets/edbc7213-939d-4d5b-b304-987a2d6b538c)
![Screenshot 2024-11-28 010819](https://github.com/user-attachments/assets/8ec32558-d44a-4f8d-ab00-bd915c74422a)
  
  Calculation of Flop Ratio :
  
  Number of D Flip Flop = 1613 Total number of cells = 14876

  Calculating Flop ratio = no.of d-flipflop / total cells
  
  _Flop Ratio_ = 1613/14876 = 0.108429685

  
</details>

## Day 2

<details>
<summary>Lab</summary>
  
``` 
run_floorplan
```
  
![Screenshot 2024-11-28 205443](https://github.com/user-attachments/assets/f32aa03b-27d1-4cd3-883c-fe745fab77f6)
  
![Screenshot 2024-11-28 210003](https://github.com/user-attachments/assets/ade4abd2-99cf-49c5-b10f-a22eb88036db)
![Screenshot 2024-11-28 2![Screenshot 2024-11-28 211601](https://github.com/user-attachments/assets/8a4758c4-d39a-4fb1-87dd-2dc6ccf87390)
10041](https://github.com/user-attachments/assets/ea276892-13f9-4599-99c6-c4545e50118a)
![Screenshot 2024-11-28 212536](https://github.com/user-attachments/assets/e5526c6f-9526-4173-b38b-aa196e5162ac)
![Screenshot 2024-11-28 213432](https://github.com/user-attachments/assets/396839ab-a57d-4f67-952e-246520396c74)

Seeing Die area
![Screenshot 2024-11-28 223040](https://github.com/user-attachments/assets/e40d4114-f139-4e86-8dc9-63dc08739594)
Steps to Open Magic

```
magic -T /home/vsduser//Desktop/work/tools/openlane_working_dir/pdks/sky130A/libs.tech/magic/sky130A.tech lef read ../../tmp/merged.lef def read picorv32a.floorplan.def &
```

![Screenshot 2024-11-28 225338](https://github.com/user-attachments/assets/25d23232-046d-4b90-8274-adbff66c4b96)
![Screenshot 2024-11-28 225645](https://github.com/user-attachments/assets/9b0785c0-7526-4d42-a2c9-b747eb0798cc)
![Screenshot 2024-11-28 230456](https://github.com/user-attachments/assets/3a0c31df-47a4-4408-998e-2e3d24b560fb)
![Screenshot 2024-11-28 230520](https://github.com/user-attachments/assets/68caf424-c5f1-4cda-be39-2facfb9de052)


</details>


## Day 3

<details>
<summary>Lab</summary>
  
```
git clone https://github.com/nickson-jose/vsdstdcelldesign
 ``` 

``` 
magic -T sky130A.tech sky130_inv.mag &
 ```
  
![Screenshot 2024-11-29 193248](https://github.com/user-attachments/assets/14b717a3-a172-4164-9f0d-8036a4b9841a)

![Screenshot 2024-11-29 193305](https://github.com/user-attachments/assets/b2983a4e-a776-4970-9381-a9f9d90ac47f)

![Screenshot 2024-11-29 193317](https://github.com/user-attachments/assets/dd3adc9e-4752-457f-8f8e-5f57296aa7fc)
Extracted the SPICE file

```
extract all
 ```

``` ext2spice cthresh 0 rthresh 0 
```

```
ext2spice
 ```

![Screenshot 2024-11-29 200843](https://github.com/user-attachments/assets/88776d55-559e-4604-8c7a-6ff890e2f812)
![Screenshot 2024-11-29 202557](https://github.com/user-attachments/assets/1ac9f862-68e6-451f-a469-b5c7c1e4fc8e)
![Screenshot 2024-11-29 203412](https://github.com/user-attachments/assets/74a8f84a-dac8-44d2-be4d-b43bbd64fcf5)
![Screenshot 2024-11-29 224130](https://github.com/user-attachments/assets/335ef237-2ccb-4873-b2e0-0d736a1166e6)

![Screenshot 2024-11-29 224609](https://github.com/user-attachments/assets/b9b00e00-c8a4-4bb5-a864-4b59d4e7a8da)

![Screenshot 2024-11-29 225015](https://github.com/user-attachments/assets/630cf2c4-49e7-4d4b-9fc4-1ef40f19daf0)

``` 
plot y vs time a
 ```

![Screenshot 2024-11-29 231631](https://github.com/user-attachments/assets/9ce104cc-a7cc-4fa9-8009-a5a0127220bb)
![Screenshot 2024-11-29 231648](https://github.com/user-attachments/assets/d665da6e-35af-4145-a26c-1d5087032ce8)
![Screenshot 2024-11-30 150815](https://github.com/user-attachments/assets/cc239838-605f-43d6-a2f3-60e990e06a1a)
![Screenshot 2024-11-30 150838](https://github.com/user-attachments/assets/c36f5b6c-b1a7-4644-89e4-32ae2dfc804a)
![Screenshot 2024-11-30 150853](https://github.com/user-attachments/assets/8de642c5-15ef-4e3f-9ec6-c80842db4414)
![Screenshot 2024-11-30 155718](https://github.com/user-attachments/assets/8a404931-864b-40e7-bbf1-5b6c3a259845)

![Screenshot 2024-11-30 155728](https://github.com/user-attachments/assets/b13ca6b8-8be3-4e3d-9038-c38b588e2d9e)
![Screenshot 2024-11-30 160544](https://github.com/user-attachments/assets/779d88cd-4e1c-4491-8a62-e11ba3484168)

![Screenshot 2024-11-30 181128](https://github.com/user-attachments/assets/d0af130e-25bf-4c80-a9f0-3bb5f8e26533)

![Screenshot 2024-11-30 233538](https://github.com/user-attachments/assets/62f5c438-c22e-4c3d-a3a4-b1d52d1bc6ba)
![Screenshot 2024-11-30 233757](https://github.com/user-attachments/assets/ce03ac75-6e53-4540-95ab-47352f89c25d)
![Screenshot 2024-12-01 000039](https://github.com/user-attachments/assets/da3da8a8-a5cb-4088-a261-762df6cab8e8)

![Screenshot 2024-12-01 001141](https://github.com/user-attachments/assets/769558ad-66b4-4dd6-892e-86698f245ce5)
![Screenshot 2024-12-01 001601](https://github.com/user-attachments/assets/4ae2638e-4aed-4858-92ed-d3430c9292ce)
![Screenshot 2024-12-01 001615](https://github.com/user-attachments/assets/1a0b2fca-25ab-4879-b705-ae72b3231252)
![Screenshot 2024-12-01 143902](https://github.com/user-attachments/assets/e91502f0-3f69-45b5-a1e0-c59cde9d8d2c)

![Screenshot 2024-12-01 144131](https://github.com/user-attachments/assets/c992ca3a-fc9f-4120-923f-8792ca574fe6)
![Screenshot 2024-12-01 153022](https://github.com/user-attachments/assets/5bc28582-b89d-4c13-9d22-a7dfed6046e5)
![Screenshot 2024-12-01 154450](https://github.com/user-attachments/assets/51bbcfe1-94a4-4ad9-9d84-a7e2a2dfbd04)
![Screenshot 2024-12-01 155254](https://github.com/user-attachments/assets/44c110f2-6e81-44aa-92ec-e93d915bfabd)
![Screenshot 2024-12-01 161450](https://github.com/user-attachments/assets/94a2718a-0015-44a0-9bb4-e450e69cf747)
![Screenshot 2024-12-01 161556](https://github.com/user-attachments/assets/235b241e-df7a-4b95-90fc-d1adf8b6d3cd)
![Screenshot 2024-12-01 161945](https://github.com/user-attachments/assets/c2256800-59ee-438d-b10d-727e7841f032)
![Screenshot 2024-12-01 164548](https://github.com/user-attachments/assets/5ad66630-bd7e-4ac8-8531-993070283e82)
![Screenshot 2024-12-01 165744](https://github.com/user-attachments/assets/ca4ab8c3-4763-40a2-9cff-0912574589f2)

![Screenshot 2024-12-01 170242](https://github.com/user-attachments/assets/38ce9451-3c40-4577-b623-1e7c033b9332)

</details>



## Day 4

<details>


<summary> Lab </summary>

Pre-layout timing analysis and Clock Tree Synthesis

```
 cd Desktop/work/tools/openlane_working_dir/openlane/vsdstdcelldesign
```
```
magic -T sky130A.tech sky130_inv.mag &
```
In tikicon window
```
help grid
```
```
help grid
```
```
grid 0.46um 0.34um 0.23um 0.17um
```


![Screenshot 2024-12-01 234324](https://github.com/user-attachments/assets/4c2131ec-fb4d-4363-9adb-3f1916142710)
```
cd Desktop/work/tools/openlane_working_dir/openlane
```
```
docker
```
```
./flow.tcl -interactive
```
```
package require openlane 0.9
```
```
prep -design picorv32a
```
```
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]
```
```
add_lefs -src $lefs
```
```
run_synthesis
```
Successfully run synthesis
![Screenshot 2024-12-02 003735](https://github.com/user-attachments/assets/d22852f4-b6ed-4135-a993-378530c2ee98)

![Screenshot 2024-12-02 004035](https://github.com/user-attachments/assets/30033976-d613-41bb-bf85-968210a4585c)

![Screenshot 2024-12-02 004047](https://github.com/user-attachments/assets/c2d1c320-a155-4e6c-9408-3d9af074051a)

![Screenshot 2024-12-04 123717](https://github.com/user-attachments/assets/251da8c3-9750-4068-9cb9-d128bc81fcf7)

![Screenshot 2024-12-04 123828](https://github.com/user-attachments/assets/e0fc5eaa-1a87-40da-bbaa-7778f37a4e2e)

![Screenshot 2024-12-04 124108](https://github.com/user-attachments/assets/c6ee1b96-b0db-4782-8932-98e9f432a4d5)

![Screenshot 2024-12-04 124122](https://github.com/user-attachments/assets/b1ba1d12-5512-4a58-9885-13ce867e9a1e)

![Screenshot 2024-12-04 124130](https://github.com/user-attachments/assets/e01bb4b8-bb9e-4697-a19c-64bcbcd82f36)

![Screenshot 2024-12-04 125025](https://github.com/user-attachments/assets/435dc095-0438-4521-b6a7-cca8a4f71cd8)

![Screenshot 2024-12-04 125717](https://github.com/user-attachments/assets/b935bd35-f603-4e6d-b340-5491375d8ab7)

![Screenshot 2024-12-04 125733](https://github.com/user-attachments/assets/a37ec3de-58d2-437b-83d0-f1af22f5bbb7)

![Screenshot 2024-12-04 125750](https://github.com/user-attachments/assets/7705b0ca-6882-45fb-8846-2462c84c7dcd)

![Screenshot 2024-12-05 211941](https://github.com/user-attachments/assets/36e186d0-f504-4dcb-9a5e-45fb22adacce)

![Screenshot 2024-12-05 212222](https://github.com/user-attachments/assets/58cc74d8-dee8-47c2-b659-96200ab723ac)

![Screenshot 2024-12-05 212457](https://github.com/user-attachments/assets/5e0cf228-ed0c-436b-b5de-065f5f04147f)

![Screenshot 2024-12-05 212514](https://github.com/user-attachments/assets/cccee3ed-48ee-4108-8f29-c862916338ea)

![Screenshot 2024-12-05 212522](https://github.com/user-attachments/assets/d8b9dd40-3cbf-440b-acfa-489cbdcbc343)

![Screenshot 2024-12-05 212538](https://github.com/user-attachments/assets/dbb0c8c1-d95b-4797-a8e3-0c676271c777)

![Screenshot 2024-12-05 213446](https://github.com/user-attachments/assets/950322e4-de41-4780-8f84-54c6f8b5afad)

![Screenshot 2024-12-05 213510](https://github.com/user-attachments/assets/95034890-a16f-4e10-af33-6d246a9b5355)

![Screenshot 2024-12-06 085501](https://github.com/user-attachments/assets/1ec92176-1c8f-4560-b5aa-245be4f5b167)

![Screenshot 2024-12-06 085643](https://github.com/user-attachments/assets/0c87d7d3-d14c-451d-8108-507fae52e432)



![image](https://github.com/user-attachments/assets/6ad1fb06-935f-43a3-833b-88c3c91b975d)

![image](https://github.com/user-attachments/assets/31ec9793-c50d-4b31-8c3d-7e1cee3bd808)

![image](https://github.com/user-attachments/assets/5a391e30-72a3-48e0-b5e6-15c495f707fe)

![image](https://github.com/user-attachments/assets/a8ab443a-5610-401c-b12c-be7e0718e530)

![image](https://github.com/user-attachments/assets/fd0acea8-c439-49fc-9694-ed497dc48e1e)

![image](https://github.com/user-attachments/assets/ad479e31-c9d9-45ec-89bc-25ce4dbc02d7)

![image](https://github.com/user-attachments/assets/2f1b884d-e269-41fe-9495-87c670e35111)

![image](https://github.com/user-attachments/assets/f96ed2f3-0345-454d-af75-5e8af58ae0b4)

![image](https://github.com/user-attachments/assets/5140d878-5f37-40e2-a16a-71f14d746c11)

![image](https://github.com/user-attachments/assets/04c6c084-277a-4726-81c2-68a30305ea0b)

![image](https://github.com/user-attachments/assets/8b7f1b9f-983e-442b-9188-7213c23bef3e)

![image](https://github.com/user-attachments/assets/d18787bd-837e-44a9-8aec-9ead5cff04fc)

![image](https://github.com/user-attachments/assets/94a52268-9544-4dcd-8dd5-c92bd899aa20)

![image](https://github.com/user-attachments/assets/176423b8-310a-4461-82f1-cb18e7192a53)

![image](https://github.com/user-attachments/assets/c011fb94-4e50-4189-b8b5-16ce00ba9cf2)

![image](https://github.com/user-attachments/assets/e5aeb9b6-9ecc-4df2-bdd5-cbe472504864)

![image](https://github.com/user-attachments/assets/58173454-c6e4-442d-952b-eac77bbb857c)



</details>

## Day 5

<details>
  <summary>Lab</summary>
  
![image](https://github.com/user-attachments/assets/c034f45c-308d-4a58-a1c6-48ac6e9f1428)

![image](https://github.com/user-attachments/assets/b7674363-3767-4bf5-8fd1-8d25b97b6936)

![image](https://github.com/user-attachments/assets/27d40f50-602b-4461-a77e-19136085db0d)

![image](https://github.com/user-attachments/assets/4fe41fdc-5b28-4e68-b6ad-71f863a79bd1)

![image](https://github.com/user-attachments/assets/f119b2ab-eabd-415f-a221-b467f54250af)

![Screenshot 2024-12-14 005932](https://github.com/user-attachments/assets/f4e41cd7-c5bb-4164-abdc-1c9b4ab9d6e4)

![Screenshot 2024-12-14 004016](https://github.com/user-attachments/assets/0bfa740b-0153-47d4-9518-d09710572f1a)


</details>


# Acknowledgements

* [Kunal Ghosh](https://github.com/kunalg123), Co-founder, VSD Corp. Pvt. Ltd.
* [Nickson P Jose](https://github.com/nickson-jose), Physical Design Engineer, Intel Corporation.
* [R. Timothy Edwards](https://github.com/RTimothyEdwards), Senior Vice President of Analog and Design, efabless Corporation.
* Google Skywater 130 PDK
* [Fayiz ferosh](https://github.com/fayizferosh/soc-design-and-planning-nasscom-vsd), Reference repository.
* [Nahusha Karnam](https://github.com/Nahusha-Karnam/SOC_Design), Reference repository.

