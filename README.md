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


<summary> Lab </summary>

![Screenshot 2024-12-01 234324](https://github.com/user-attachments/assets/4acb3432-1e4f-4361-87cd-51041f995dc7)

![Screenshot 2024-12-02 003735](https://github.com/user-attachments/assets/b3ea7d62-a3a1-4a94-9764-72572fc417c7)

![Screenshot 2024-12-02 004035](https://github.com/user-attachments/assets/a27d53dc-7765-4496-9178-5e9c4c92e94a)

![Screenshot 2024-12-02 004047](https://github.com/user-attachments/assets/04b775cc-d2cf-4145-a186-dba1cbd5f804)

![Screenshot 2024-12-04 123717](https://github.com/user-attachments/assets/8cc9ffd8-c8d2-4d66-9f59-770c833ab122)

![Screenshot 2024-12-04 123828](https://github.com/user-attachments/assets/85b002ac-0293-442b-9a74-c35ed4adaa64)

![Screenshot 2024-12-04 124108](https://github.com/user-attachments/assets/813ec20e-e37f-4573-8308-cbc5815071c4)

![Screenshot 2024-12-04 124122](https://github.com/user-attachments/assets/ad160f12-1562-4d66-abb6-fa5c6c19fc5d)

![Screenshot 2024-12-04 124130](https://github.com/user-attachments/assets/30e15ff4-6067-49f1-8351-daba3b1fcdac)

![Screenshot 2024-12-04 125025](https://github.com/user-attachments/assets/35ab5a58-0359-4284-a103-0b2b97912f22)

![Screenshot 2024-12-04 125717](https://github.com/user-attachments/assets/e72b0f8b-08f0-4a80-98da-bef1233fad5e)

![Screenshot 2024-12-04 125733](https://github.com/user-attachments/assets/81028d97-7917-4222-b681-fcd4da6d9f12)

![Screenshot 2024-12-04 125750](https://github.com/user-attachments/assets/32e0927e-0686-4786-9b76-3d5d3b17e875)

![Screenshot 2024-12-05 211941](https://github.com/user-attachments/assets/8c2ff4d0-f136-43f5-9f24-2881568178f0)

![Screenshot 2024-12-05 212222](https://github.com/user-attachments/assets/7d74016d-fbff-453c-97ea-6d3d5133209a)

![Screenshot 2024-12-05 212457](https://github.com/user-attachments/assets/112fccf7-2fb6-4417-a737-1ee39187df69)

![Screenshot 2024-12-05 212514](https://github.com/user-attachments/assets/da94a00b-24f3-466a-be9a-d10bcfb7737f)

![Screenshot 2024-12-05 212522](https://github.com/user-attachments/assets/f2b8ca4d-13fc-4d9c-bd65-949c66ac8db6)

![Screenshot 2024-12-05 212538](https://github.com/user-attachments/assets/65146172-2742-4434-a44c-9f5a8e000e20)

![Screenshot 2024-12-05 213446](https://github.com/user-attachments/assets/eab2cd83-f0f1-42cb-afca-1bac8d34e874)

![Screenshot 2024-12-05 213510](https://github.com/user-attachments/assets/e666c34c-a960-4388-a356-238aced5a2a7)

![Screenshot 2024-12-06 085501](https://github.com/user-attachments/assets/e94918a8-2021-4f1f-936d-516fd41bb953)

![Screenshot 2024-12-06 085643](https://github.com/user-attachments/assets/58eceec0-8aff-401c-8d72-17cfcf565845)

</details>
